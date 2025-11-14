# Club-Wide Project Tracker

**Welcome to the Cyranch CS Club Project Hub!** This repository is where we propose, discuss, vote on, and track club projects.

> Note: in the beginning, this process may be changing frequently till hiccups and issues are ironed out. Changes will settle as time marches on, but we're basically in an **alpha stage**.

## How to Vote on Projects

Vote on projects you'd like to work on by **assigning yourself** to their corresponding issues in our [GitHub Project Board](https://github.com/orgs/cyranch-csclub/projects/2/views/1).

- **You can vote on multiple projects** - Show interest in as many as you'd like!
- **Your vote matters** - Projects with more support are more likely to get greenlit
- **Voting is ongoing** - You can change your votes as projects evolve

> Remember, changing anybody else's assignment is *against club rules* and will get you *removed from the organization* and may cause all members' default permissions to be narrowed. So don't do it, even as a joke.

## Active Projects

Each active project has:
- A markdown file in the `/projects` folder describing the project
- An associated issue for discussion and voting
- A project proposal that has been approved by an officer

**Browse active projects:** Check the `/projects` folder or see the [GitHub Project](https://github.com/orgs/cyranch-csclub/projects/2).

## Proposing a New Project

Have an idea? Here's how to propose it:

### 1. Create Your Proposal

To get your idea across, you should make a proposal. The details can be barebones initially, but it has to be fleshed-out before getting approved.
Create a markdown file in the `/proposals` folder using this template:

**Filename:** `your-project-name.md`

**Template:**
```markdown
# Project Title

## Proposer
Your Name (Discord Username)
You can put your GitHub username here in lieu of your name if preferred.

## Overview
A brief 2-3 sentence description of what this project is.

## Proposed Tech Stack
- Language(s)
- Framework(s)
- Tools/Libraries

## Prerequisites/Skills Needed
What skills should contributors have or be willing to learn?

## Details
The fine details of the project.
What would the intended end product look like?
What would the process of development be?
Etc.

## Open Questions
Anything you're unsure about or want/would like feedback on?
```
> Note: This template is a *guide*. Other than the proposer, everything else can be changed - but a more detailed and thorough a proposal is, the more efficiently work can be done on it, and the faster it will be before it is greenlighted.

### 2. Submit Your Proposal

1. Create your markdown file in the `/proposals` folder
2. Commit and push it to the repository
3. Create a new issue with:
   - Title: Your project name
   - Content: Copy/paste your proposal or link to the markdown file, or make something else.
4. Assign yourself to the issue to show your support for it.

Once you open the issue, it should automatically be added to our Project and marked as `Proposed` (it may take a few seconds).

### 3. Gather Feedback

- Respond to comments and questions on your issue
- Update your proposal markdown file based on feedback
- Build consensus around the idea
- Discuss in Discord to refine your proposal

### 4. Approval Process

Once your proposal has:
- Sufficient community interest (people assigning themselves to the issue)
- A clear, feasible plan
- Officer approval

An officer will:
1. Move your proposal from `/proposals` to `/projects`
2. Change the issue status from `Proposed` to `Todo`.
3. Create a dedicated repository for the project
4. Set up the project on the project board (will change status to `In Progress`)
5. Announce that work can begin!

## Guidelines & Rules
Do NOT:
- modify a project's status, whether in the Project Board or by moving your proposal between the folders.
- change anybody's assignment/vote
- edit anybody's proposal without their permission
- clone or close issues that aren't yours
- spam
- propose projects that you have no intention of working on
- alter this repository and the Project Board in any other way (including messing with the organization structure)

What you CAN do:
- Make new proposals
- Assign yourself to show interest
- Open issues regarding the repository's content
- Comment on existing issues
- Follow the spirit of these guidelines to have a clean and efficient process.

You may have the *ability* to do things beyond the list above (due to repo permissions), but violation of the rules can result in you being removed from the organization.

## Discussion & Questions

**Discussing Projects:**
- Comment on project issues to ask questions, suggest improvements, or coordinate
- Discussion is **strongly encouraged** - great projects come from collaboration!
- Only the project proposer (or officers) should edit the project markdown file
- Significant changes to a project should be discussed in the issue first

**General Questions:**
- Open a new issue with the `question` label
- Ask in the Discord server
- Assign yourself to existing `question` issues if you have the same question

## Repository Structure
```
/
├── README.md           # This file
├── proposals/          # Pending project proposals
├── projects/           # Approved, active projects
└── archive/            # Completed or inactive projects
```

## Project Lifecycle
```
Proposal → Discussion → Approval → Active Development → Completion/Archive
```

1. **Proposal Stage** - Idea submitted in `/proposals`, being refined
2. **Discussion Stage** - Community feedback and iteration via issue comments
3. **Approval Stage** - Officers review and approve
4. **Active Development** - File moved to `/projects`, work happens in dedicated repo
5. **Completion** - Project finished, moved to `/archive`

## FAQ

**Q: Can I work on a project without voting on it?**  
A: Yes! Voting just shows interest. You can join any active project's repository.

**Q: What if my proposal isn't getting traction?**  
A: Keep discussing it! Sometimes proposals need time to develop. Ask for feedback in Discord.

**Q: Can I propose multiple projects?**  
A: Absolutely! Just make sure you can commit time to them if approved.

**Q: How do I know which projects need help?**  
A: Check the project board and look for issues with the `help-wanted` label.

**Q: Can projects be modified after approval?**  
A: Minor updates yes (edit the markdown). Major pivots should be discussed with the team and officers first.

**Q: What happens to rejected proposals?**  
A: They stay in `/proposals` with feedback. You can revise and reopen discussion, or they may eventually be moved to `/archive`.

## Contributing

This is a collaborative space! We value:
- Constructive feedback
- Creative ideas
- Respectful discussion
- Active participation

**Don't forget:** You can comment on any proposal to help shape it into something amazing!

---

**Let's build something amazing together!**
