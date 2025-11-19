# Member page on Club Website

## Proposer
Shubh R. (acemavrick)


## Goal
To create a page/section on the club's website that would list all the current members of this GitHub organization,
and would automatically update when members are added or removed. 

## Proposed Tech Stack
- HTML, CSS for the website
- YAML for GitHub Actions
- TypeScript for Cloudflare workers
- (?) Astro for the website

## Details

There exists an [API to list organization members](https://docs.github.com/en/rest/orgs/members?apiVersion=2022-11-28#list-organization-members), but it cannot be put in the website itself (doing so would cause heavy rate limiting). 
Instead, we can have a **webhook** that would trigger on member list changes, attach that webhook to a **Cloudflare worker** which then triggers a **GitHub Action** that uses the **API** to build a static page, which it then deploys to **GitHub pages**.

The webhook would be configured to make a POST request upon member additions or member deletions, by enabling the [`organization` event](https://docs.github.com/en/webhooks/webhook-events-and-payloads?actionType=member_added#organization).

The webhook would post to a [**Cloudflare worker**](https://workers.cloudflare.com/), which would authorize the request and filter it. Since the `organization` event includes more events than just member addition/deletion, this filtering step is required. If the event gets through the authentication and filter, the worker can issue a [repository dispatch event](https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#create-a-repository-dispatch-event) which would trigger the GitHub workflow.

We'd have two GitHub actions that need to be run in the same workflow. A *workflow* gets one VM, and it can run multiple actions. We'd first use the API to list members to download a `members.json` in VM memory. Then, we'd build the site using Astro or some other framework (that would use `members.json` as a template) and then deploy it to GitHub pages. The workflow would be triggered by a [`repository_dispatch` event](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#repository_dispatch) with an event type of `member_list_change` (custom event type, sent by the worker). 

In summary, the process is as follows: <br>
Member added/removed --> webhook triggered --> Cloudflare worker triggerd --> GitHub workflow triggered --> site deployed.

### Areas to Contribute
* Creating the GitHub workflow (backend)
* Setting up the club website to use Astro (backend)
* Writing the member page (heavy frontend)
