# SC2006-Lab-Group-Project-SCSD

This outlines the standard Git Workflow, branching strategy and contribution rules to ensure smooth collaboration

## 1. Branching Strategy 

* **`Main` :** The stable production branch. This represents the stable releases or production-ready code. **DIRECT COMMITS STRICTLY PROHIBITED**
* **`Dev`:** The integration branch and all ongoing in progress works from our feature branches, bug fixes, and testing will occur here before we merge into the Main Production.
* **`Feature Branch`:** Individual Branches for developing features or fixing bugs

--

## 2. Do or Don'ts

### **DO:**

 * **DO** Create a dedicated feature off the `dev` branch for every single task or bug fix you work on.
 * **DO** Pull the latest changes from the base development branch before merging your code back to avoid overwrite conflicts.
 * **DO** Write Clear, Descriptive commit messages so team members can understand the context of your changes

 ### **DON'Ts**

 * **DON'T** Push the code directly to `main` or `dev`. Always merge from `feature` branch -> `dev` via pull requests
 * **DON'T** Ignore merge conflicts; resolve them locally or discuss on the conflicts before finalizing a merge to prevent any dispute

## 3. Standard Git Workflow & Command References

### Step 1: Switch to `dev` and create your feature branch
Ensure you are up to date on the development branch and spin up your isolated workspace.

```bash
git checkout dev
git checkout -b featureABC
```

### Step 2: Make changes, commit then push
Stage your changes locally and push them to the remote repository
```bash
git commit -m "commit message"
git push origin feature/hougang-abc
```

### Step 3: Sync before integrating
Before merging or submitting your changes back, pull the latest updates from the remote base branch to ensure compatibility
```bash
git pull origin feature/hougang-abc
```

### Step 4: Combine and merge
Combine multiple commits into a single clean commit using a squash merge when moving back into the target branch
```bash
git merge --squash dev
```
