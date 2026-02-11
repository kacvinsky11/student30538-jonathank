# PPHA 30538: Data Analytics and Visualization for Public Policy
## Winter 2026
## University of Chicago Harris School of Public Policy
## Peter Ganong and Maggie Shi

# Minilesson Recordings

Found [here](https://uchicago.app.box.com/folder/359280505901?s=zdgwdq3hrg0d888pwexrjb9matlaocq3), too big to push to the student repo

# Repository Structure

Lectures are stored in the `lectures` folder. Within each folder, each lecture will have its own folder with slides. 
Each problem set and mini-lesson will have their own folders within their respective folders. 

---
# Accessing the Repository
## Step 1: Fork the Repository  
- Go to the [original repository](https://github.com/uchicago-harris-dap/student30538-w26) on GitHub.  
- Click the **Fork** button in the upper-right corner of the repository page. This will create a personal copy of the repository in your GitHub account.

---

### Step 2: Clone Your Forked Repository  
1. In your GitHub account, navigate to your **forked repository**.  
2. Click the green **Code** button and copy the **HTTPS URL**, **https://github.com/uchicago-harris-dap/student30538-w26**.  
3. Open a terminal and run the following command:
   ```bash
   git clone https://github.com/uchicago-harris-dap/student30538-w26
   ```

### Step 3: Set the Upstream Remote  
(Optional but recommended to keep your fork updated.)  
1. Navigate to the cloned repository in your terminal:
   ```bash
   cd student30538-w26
   ```
2. Add the upstream remote:
   ```bash
   git remote add upstream https://github.com/uchicago-harris-dap/student30538-w26
   ```
3. Confirm your remotes:
   ```bash
   git remote -v
   ```

### Step 4: Sync Your Fork with the Original Repository  
1. Fetch updates from the original repository:
   ```bash
   git fetch upstream
   ```
2. Merge the updates into your local branch:
   ```bash
   git merge upstream/main
   ```
   Replace `main` if the default branch has a different name (e.g., `master`).


---

## Setting up your environment

1. `cd` into the repository
2. Create **and/or** activate the Conda environment named **dap**, then install the Python dependencies listed in `environment.yml`:
   ```bash
   conda env create -n dap -f environment.yml   # first‑time setup
   conda activate dap                            # run this every time you work on the repo
   ```

---

## Registering the Jupyter kernel

Quarto’s **Preview** button in VS Code launches a Jupyter kernel whose name is defined in `_quarto.yml` (`jupyter: dap`). Register that kernel once per machine so Quarto always finds the *dap* Conda environment regardless of local paths:

```bash
conda activate dap               # ensure the env is active
python -m ipykernel install \
       --user \
       --name dap \
       --display-name "dap"
```

After this step `jupyter kernelspec list` should include a line like:

```
dap          /Users/…/Library/Jupyter/kernels/dap
```

---

## Install Quarto and Jupyter Extension
1. Open VS Code  
2. Open Extensions (`Cmd + Shift + X` on Mac, `Ctrl + Shift + X` on Windows)  
3. Search for **Quarto**  and install (publisher: Quarto)
4. Search for **Jupyter**  and install (publisher: Microsoft)  
5. Restart VS Code  


Feel free to reach out via EdDiscussion if you have any questions or run into any issues. Happy coding!
