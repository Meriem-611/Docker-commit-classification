# Annotation Guidelines for Docker Commit Messages

## Overview
Your task is to classify each commit message into one or more of the following categories:
- **Bug Fix**
- **Feature Addition**
- **Code Refactoring** (with specific Docker techniques)
- **Maintenance**
- **Not Enough Information**

In some cases, a commit might fit into more than one category. You are allowed to assign multiple labels if necessary. Additionally, if the commit message alone doesn't provide enough information, you will be asked to inspect the code changes before and after the commit to finalize the labeling.

For reference, I have labeled the first 20 commit examples. These are available as a guide to help you understand how to apply the labels.

---

## Labels and Definitions

### 1. **Bug Fix**
- **Definition**: A commit that resolves known bugs or issues in the code.
- **Keywords**: `fix`, `bug`, `patch`, `error`, `issue`.
- **Example**: "Fix memory leak in Docker container."
  - **Label**: Bug Fix
  - **Why**: This commit addresses a known bug by fixing a memory leak.

### 2. **Feature Addition**
- **Definition**: A commit that introduces new functionality, tools, or support.
- **Keywords**: `add`, `new`, `introduce`, `support`.
- **Example**: "Added support for gvt and good builds."
  - **Label**: Feature Addition
  - **Why**: The commit adds new support for build systems, indicating a feature addition.

### 3. **Code Refactoring** (Docker-Specific Techniques)
- **Definition**: A commit that improves code structure without changing external behavior, focusing on performance, maintainability, or optimization.
- **Docker-specific techniques**:
  - **Sort Instructions**: Reordering Dockerfile instructions to optimize build efficiency.
  - **Combine RUN**: Merging multiple `RUN` commands to reduce layers.
  - **Update Base Image**: Changing the base image for better performance or security.
  - **Optimize Instructions**: Improving commands for performance, such as using `--no-cache`.
  - **Remove Unnecessary Files**: Deleting temporary files post-installation to reduce image size.
- **Keywords**: `refactor`, `optimize`, `simplify`, `restructure`, `update`, `sort`, `multi-stage`, `reduce`
- **Example**: "Install packages without caching the index."
  - **Label**: Code Refactoring
  - **Why**: This refactoring optimizes the Dockerfile by preventing unnecessary caching during installation.

### 4. **Maintenance**
- **Definition**: Non-functional updates such as version bumps, merges, or dependency updates.
- **Keywords**: `bump`, `version`, `merge`.
- **Example**: "Bumped source to 20211031-27d752c."
  - **Label**: Maintenance
  - **Why**: This commit is a version bump, typical for maintenance.

### 5. **Not Enough Information**
- **Definition**: If the commit message does not provide enough information to determine a label confidently or if not sure, the annotator should inspect the code before and after the commit.
- **Example**: "rev 741675."
  - **Label**: Not Enough Information
  - **Why**: The message lacks detail, so the code must be reviewed to assign a label.

---

## Steps for Annotation:
1. **Review the Commit Message**: First, examine the commit message and assign one or more labels based on the definitions above.
2. **Select "Not Enough Information"** if you cannot confidently label the commit based on the message alone.
3. **Review the Code (If Needed)**: If "Not Enough Information" was selected, inspect the code changes (before and after the commit) to finalize the labeling.
4. **Apply Multiple Labels if Necessary**: If the commit fits more than one category (e.g., it both fixes a bug and refactors the code), assign all relevant labels.

---

## Examples

- **Commit**: "Install packages without caching the index."
  - **Labels**: Code Refactoring, Maintenance
  - **Explanation**: This commit optimizes the Dockerfile and may also involve minor maintenance.

- **Commit**: "Fix Dockerfile permission issue."
  - **Label**: Bug Fix
  - **Explanation**: The commit resolves a specific issue in the Dockerfile related to file permissions.

- **Commit**: "Added support for multi-stage builds."
  - **Label**: Feature Addition
  - **Explanation**: A new feature is introduced by adding multi-stage build support.

---

## Contact Information
If you have any questions or face issues during the labeling process, feel free to contact meriemm@umich.edu .
