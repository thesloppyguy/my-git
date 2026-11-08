# My Git

**A Git-compatible, next-generation version control system written in Rust.**

My Git is an extensible version control solution built on top of Git's ecosystem, combining the reliability and interoperability of Git with the modern workflow capabilities of Jujutsu and ideas from Mercurial.

It aims to make version control more intuitive, secure, flexible, and better suited to modern software development — particularly collaborative development and AI-assisted engineering.

My Git is the first component of a larger `my-*` tooling ecosystem, currently under development. Version control comes first because it forms the foundation for project management, development workflows, and collaboration.

---

## Vision

Git is an incredibly powerful version control system, but many of its workflows are difficult to learn, unnecessarily complex, or poorly suited to modern development practices.

My Git aims to preserve everything that makes Git successful while improving the developer experience around it.

The guiding principle is simple:

**Keep Git's compatibility. Improve everything around it.**

My Git should allow developers to continue using their existing repositories, remotes, CI pipelines, Git hosting providers, IDEs, and established workflows without requiring changes to their infrastructure.

At the same time, it should introduce capabilities that make version control more powerful:

- More intuitive history management.
- Better conflict resolution.
- First-class undo and redo.
- Secure handling of sensitive files.
- More flexible commit and PR workflows.
- Native support for AI-assisted development.
- Isolated background development environments.

---

## Core Principles

### 1. Git Compatibility First

Git compatibility is a foundational requirement, not an optional feature.

- Work with standard Git repositories.
- Support existing Git remotes and hosting platforms.
- Preserve compatibility with GitHub, GitLab, Bitbucket, and self-hosted Git servers.
- Maintain compatibility with existing Git CI/CD pipelines and workflows.
- Allow interoperability with standard Git CLI commands and tooling.
- Avoid introducing proprietary repository formats or mandatory infrastructure.

### 2. Developer Experience

Make complex version control operations easier without removing the underlying power.

- Intuitive command-line interface.
- Improved history visualization.
- Simplified branching and rebasing workflows.
- Better conflict resolution.
- Easy-to-understand undo and redo.
- Flexible commit management.

### 3. Security by Design

Sensitive data should be manageable without compromising the usability or interoperability of a repository.

- Encrypted files and directories.
- Environment file management.
- Private file and directory policies.
- Encryption key management.
- Secure collaboration and key sharing.
- Protection against accidental secret exposure.

### 4. AI-Native Development

Version control should become an active part of AI-assisted software development.

- AI-generated development checkpoints.
- Recoverable agent sessions.
- Isolated AI development workspaces.
- Context-aware history and change inspection.
- Agent-accessible repository operations.
- Safe experimentation and rollback.

### 5. Extensibility

My Git should be designed as a foundation for future development tooling.

- Modular architecture.
- Extensible command system.
- IDE and editor integrations.
- Machine-readable interfaces.
- APIs for external tools and agents.

---

## Feature Set

### 1. Core Version Control

Complete Git functionality with compatibility as the primary objective.

- Repository initialization and management.
- Staging and working tree management.
- Commits and history.
- Branches and tags.
- Merge and rebase.
- Fetch, pull, push, and remote management.
- Diff and patch operations.
- Stash management.
- Cherry-pick and revert.
- Submodules and Git LFS interoperability.
- Git configuration and hooks.
- SSH and HTTPS authentication.

### 2. Improved Version Control Workflows

Bring modern version control concepts into the Git ecosystem.

- First-class undo and redo.
- Flexible commit creation and modification.
- Change-based history management.
- Better conflict detection and resolution.
- Interactive history editing.
- Automatic recovery points.
- Improved commit splitting and consolidation.
- Better PR preparation and commit organization.
- More intuitive branch and change management.

### 3. Sensitive File Management

Introduce secure file management without disrupting standard repository workflows.

**Environment files**
- Native `.env` support.
- Encrypted environment file storage.
- Multiple environment configurations.
- Secure environment file synchronization.
- Environment-specific access controls.

**Encrypted files and directories**
- File-level encryption.
- Directory-level encryption.
- Encrypted repository content.
- Automatic encryption and decryption.
- Key management and rotation.
- Secure sharing of encrypted content.

**Private file and directory policies**

Allow developers to mark files and directories as private, even within publicly hosted repositories.

- Private file and directory declarations.
- Configurable visibility policies.
- Encryption-backed protection for sensitive content.
- Local-only files and directories.
- Rules for handling private content during commits and pushes.

The objective is to support mixed-visibility repositories without forcing developers to split projects across multiple repositories.

### 4. Advanced Development Workflows

- Background worktrees.
- Isolated development environments.
- Parallel feature development.
- AI development checkpoints.
- Automatic checkpoint creation.
- Easy recovery from failed experiments.
- Independent agent workspaces.
- Worktree lifecycle management.

### 5. Developer Integrations

- Git-compatible CLI.
- Machine-readable command output.
- IDE integrations.
- Git graph and history visualization.
- Agent and automation interfaces.
- Repository management APIs.
- GUI integration points.

---

## Technology and Design References

My Git draws inspiration from established version control systems, adopting their strongest concepts rather than attempting to reinvent proven solutions.

| Project | Concepts to draw inspiration from |
|---|---|
| Git | Repository format, object model, remotes, interoperability, ecosystem |
| Jujutsu (`jj`) | Change-oriented workflows, automatic snapshots, operation history, conflict handling |
| Mercurial | User experience, revsets, extensible architecture, history management |

These projects are references, not implementation dependencies or mandatory architectural choices.

The implementation will be written in Rust, prioritizing performance, safety, reliability, and maintainability.

### Architectural Direction

My Git will initially operate on standard Git repositories.

The architecture should separate:

- **Core engine:** Repository operations and version control primitives.
- **Git compatibility layer:** Git object model, references, index, remotes, and interoperability.
- **Workflow engine:** Improved history management, undo/redo, changes, and conflict resolution.
- **Security engine:** Encryption, decryption, privacy policies, and key management.
- **Workspace engine:** Worktrees and isolated development environments.
- **Integration layer:** CLI, APIs, IDEs, and AI agents.

This separation should allow new capabilities to evolve without compromising Git compatibility.

---

## Development Roadmap

### Phase 1 — Git Compatibility and Foundation

**Objective:** Establish a reliable Git-compatible foundation.

- Rust-based core architecture.
- Repository initialization and management.
- Git object model and reference management.
- Working tree and index operations.
- Commit and history management.
- Branch and tag management.
- Merge and rebase.
- Remote synchronization.
- Git CLI interoperability.
- GitHub and GitLab compatibility.
- CI/CD and hook compatibility.

**Milestone:** My Git can operate on standard Git repositories and support everyday development workflows without breaking existing infrastructure.

### Phase 2 — Modern Version Control Workflows

**Objective:** Introduce the best ideas from Jujutsu and Mercurial.

- Change-oriented history management.
- Automatic working copy snapshots.
- Operation history.
- Undo and redo.
- Improved conflict management.
- Flexible commit management.
- Commit splitting and consolidation.
- Interactive history editing.
- Improved PR preparation.
- Background worktree primitives.

**Milestone:** Developers can use My Git for everyday work and benefit from modern version control workflows while retaining Git interoperability.

### Phase 3 — Security and Sensitive Data Management

**Objective:** Make sensitive data a first-class part of repository management.

- Environment file support.
- File and directory encryption.
- Private file and directory policies.
- Local-only file management.
- Encryption key management.
- Key rotation and recovery.
- Secure sharing.
- Automated encryption and decryption.
- Protection against accidental secret exposure.

**Milestone:** Developers can manage source code and sensitive project data within the same repository while maintaining explicit security boundaries.

### Phase 4 — AI-Native Development and Integrations

**Objective:** Make My Git a foundational component of AI-assisted development.

- AI development checkpoints.
- Agent-specific workspaces.
- Background worktree management.
- Agent-accessible repository operations.
- IDE integrations.
- Git graph visualization.
- Change and history exploration interfaces.
- GUI actions.
- Machine-readable APIs.
- External tool integrations.

**Milestone:** AI agents and developers can safely collaborate, experiment, recover, and manage changes through a shared version control foundation.

---

## Compatibility Guarantees

Git interoperability is a core product requirement.

My Git should aim to ensure:

- Standard Git repositories remain readable by Git.
- Existing Git remotes remain usable.
- Standard Git clients can interact with My Git repositories.
- GitHub and GitLab workflows remain unaffected.
- CI pipelines do not require My Git-specific modifications.
- Existing repository history is preserved.
- My Git-specific metadata does not interfere with standard Git operations.

Any feature that cannot be represented natively in Git should use a clearly separated compatibility mechanism.

---

## Non-Goals

My Git is not intended to:

- Replace Git hosting platforms.
- Require a proprietary remote server.
- Force developers to abandon existing Git tooling.
- Introduce an incompatible repository format.
- Require AI functionality for normal version control operations.
- Sacrifice reliability for convenience.

The initial focus is local-first version control with seamless remote interoperability.

---

## Project Status

My Git is under active development.

The initial focus is establishing the Rust architecture and Git compatibility foundation before introducing higher-level workflows and security features.

The long-term objective is to build a reliable, extensible version control foundation for the broader `my-*` developer tooling ecosystem.

---

> **My Git — Git compatibility, without Git's limitations.**