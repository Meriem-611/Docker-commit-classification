# README: Filtered Docker Commit Messages Dataset for Classification

## Dataset Overview
This dataset contains commit messages from Docker-related projects. The original dataset, [BigCode's commitpack dataset](https://huggingface.co/datasets/bigcode/commitpack), had **259,379 data points**. However, due to time constraints for manual labeling, the dataset has been filtered down to **5,000 commit messages** that are specifically related to Dockerfile changes.

## Source of Data
- **Original Source**: The dataset was sourced from BigCode's commitpack dataset, which contains millions of commit messages from various repositories. I specifically filtered Docker-related commit messages for this task.
  
- **Filtered Dataset**: The commit messages were filtered based on keywords such as **"fix"**, **"add"**, **"refactor"**, and **"bump"** to categorize the messages into bug fixes, feature additions, code refactorings, and maintenance tasks.

## Dataset Structure
The dataset is stored in a **Google Sheet**, where each row represents a commit message. The following columns are included:
- **Commit Hash**: The unique identifier for each commit.
- **Subject**: A short summary of the commit message.
- **Message**: The full commit message, if available.
- **Old File/New File**: Files before and after the commit.
- **Old Contents/New Contents**: The content of the files before and after the commit.
- **First Labeling Column**: Annotators use this column to label the commit based on the commit message alone.
- **Second Labeling Column**: If the annotator selects **"Not Enough Information"** in the first pass, they can re-label after reviewing the code changes.

## Number of Instances
- **Original Dataset**: 259,379 commit messages.
- **Filtered Dataset**: 5,000 commit messages were selected for manual labeling.

## Filtering Process
The dataset was filtered down to 5,000 instances to ensure efficient manual labeling. The commit messages were filtered based on specific keywords relevant to the classification task:
- **Bug Fixes**: Filtered using keywords like "fix", "bug", "resolve".
- **Feature Additions**: Filtered using terms like "add", "new", "feature".
- **Code Refactoring**: Filtered using words such as "refactor", "optimize", "simplify".
- **Maintenance**: Filtered using terms like "bump", "merge", "upgrade".

## Estimated Labeling Time
- Each item can be labeled in approximately **15-30 seconds** based on the commit message alone.
- If the annotator needs to review the code before and after the commit, labeling may take around **1-2 minutes** per item.

## License
This dataset is shared under the **MIT License**, allowing for reuse, modification, and distribution, provided that proper attribution is given.
