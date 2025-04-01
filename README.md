# game-ini
A repository to track the `Game.ini` changes for __*The HELL: City Builder of the Undead*__.  
This repo ensures version control for key gameplay parameters, balancing decisions, and experimental configurations across development stages.

## Purpose
This repository exists to:
- Track iterative changes made to the `Game.ini` file.
- Maintain a historical record of balance decisions.
- Allow quick rollback to previous states during testing.
- Document rationale behind specific tuning or changes.

## Branching Guidelines
`main` branch __(Production Safe)__
<br /><br />
This branch is protected and can not be changed without a Pull Request (PR) / Merge Request (MR). The PR / MR has to be approved by MIS before it can be merged. The contents of this branch is __ALWAYS SAFE FOR PRODUCTION__.

---

`dev` branch __(Stable, Developer Iterations)__
<br /><br />
This branch is used to facilitate development. This branch is intended to serve users to continue their development for the latest copy. When one needs to update the Game.ini file, they should begin either by __branching from the `dev` branch into a separate branch__ or __commit a straightforward, slightly changed update__ of the Game.ini file.

---

`*` branch __(Experimental, Always Branching from `dev`.)__
<br /><br />
You are free to create as many branches from `dev` as you want. These branches will serve as experimental or development purpose. __IT IS YOUR RESPONSIBILITY__ to ensure your change in these branches are published and merged in to `dev` and then subsequently ensure that your changes make its way up to `main`.

## Merging Guidelines
`main` branch
<br /><br />
Pull Request (PR) / Merge Request (MR) is required to publish your changes to the `main` branch. __ALL__ the commits in your MR / PR has to follow the commit guidelines.

## Commit Messages Guidelines
Follow these rules for all commits to maintain a clean and informative history:
- __ALWAYS__ use lower case alphanumeric characters __ONLY__.
    + Why?
        * Because upper case is to be reserved for system events and system forced commits.
        * Do __NOT__ use symbols within your commit messages at all. Git works within the Linux ecosystem where symbols are reserved characters. Your Git GUI may misinterpret symbols and ultimately mess up the commit. By not using symbols in your commit message, you eliminate this risk completely.
- __ALWAYS__ start your commit messages with the verbs; __*added, updated or removed*__.
    + Why?
        * This allows your collaborator to understand the change in 1 word. All subsequent word of this commit will support "added", "updated" or "removed".
- __ALWAYS__ restrict the summary of your commit message to one line.
    + Why?
        * Commits should be short and frequent. Do __NOT__ nest multiple unrelated changes in one commit. This will also make rolling back the code easier.
- __ALWAYS__ leave One (1) line space before entering your commit in point form. Denote each point with the "-" character.
    + Why?
        * Git convention denotes that the first line of the message is the description of your commit. Leaving one line, then comes the body.
        * __MOST__ GUI tools displays the information based off the conventions set by Git. Breaking the convention can cause search and display issues.

---

### Example Commit Messages:
These examples below follow all the guidelines above. Refer back to these examples whenever you are unsure about how to write you commit message.

#### Addition (Small Change, Single Line Commit Message, Description Only)
```added titan settings```

#### Addition (Big Change, Multiple Line Commit Message, Description and Body)
```
added multiple unit settings

- added sentry settings
- added siren settings
- added stalker settings
- added sinner settings
```

---

#### Update (Small Change, Single Line Commit Message, Description Only)
```updated soul movement speed```

#### Update (Big Change, Multiple Line Commit Message, Description and Body)
```
updated stage 1 configurations

- increased number of souls spawned in mission 1
- updated all earthquake events 1 second longer
- removed deprecated soul movement configurations
```

---

#### Remove (Small Change, Single Line Commit Message, Description Only)
```removed redundant graphic settings```

#### Remove (Big Change, Multiple Line Commit Message, Description and Body)
```
removed some stage 1 configurations

- removed hauler and labour cofigurations
- removed slitter turning chance
```
