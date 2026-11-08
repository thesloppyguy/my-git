# My Git

The goal of this project is to implement my own git wrapper in rust. The following are the table stakes for the current solution.

- Base Git functionality
- Env file support
- Encrypted file / dir support
- Labeling dir and files as private on a public repo
- Git CI and workflows remain uneffected
- Better conflict management
- Better commit breakdown for PRs
- redo / undo
- AI Checkpoint support
- Background worktrees

This project will be part of a bigger `my-*` project still under development. We are starting with virsion control as its the core of project management.

---

For this project we will be taking reference from existing solutions as to not reinvent the wheel, the projects are listed below.

- git
- jj
- Mercurial

We plan to combine the best of all these solutions and implement a backwards compatible solution in rust.

Ironically enough to get started with this project I am using git as the version control system and TUI.
