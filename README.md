# GH-FOSS-T1: Make a commit and open a PR

## What you’ll do

You’ll add your name and roll number to `participant.md`, save that change as a **commit**, and ask the maintainers to merge it using a **pull request (PR)**.

## 1. Fork the repository

1. Open the original repository on GitHub.
2. Click **Fork** at the top right.
3. Create the fork under your GitHub account.

You’ll now have your own copy here:

```text
https://github.com/<your-username>/<repo-name>
```

## 2. Clone your fork

Open a terminal and clone **your fork**:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

Example:

```bash
git clone https://github.com/LooninS/foss-workshop.git
cd foss-workshop
```

## 3. Get the latest changes

Make sure your copy is up to date:

```bash
git pull origin main
```

If the project uses `master` instead of `main`, use:

```bash
git pull origin master
```

GitHub usually names the default branch `main`, while older Git setups often use `master`.

## 4. Create your own branch

Don’t commit directly to `main`. Make a  branch for your change:

```bash
git switch -c add-my-details
```

You can also use your username:

```bash
git switch -c add-<username>-participant
```

## 5. Add your details

Open `participant.md` and add your details in the same format as everyone else.

For example:

```md
Sourish: IIT2025099
```

Please don’t edit anyone else’s entry.

## 6. Check what you changed

Run:

```bash
git status
```

Make sure only `participant.md` was changed and your details look correct.

## 7. Save your change

Stage the file:

```bash
git add participant.md
```

Then commit it:

```bash
git commit -m "Add my details to participant.md"
```

A good commit message briefly says what you changed.

## 8. Upload your branch

Send your branch to GitHub:

```bash
git push origin add-my-details
```

The first time you push, GitHub may ask you to log in. Using **SSH** is recommended so you don’t need to create a personal access token every time.

## 9. Open the pull request

1. Go to your fork on GitHub.
2. You’ll usually see a yellow banner saying **Compare & pull request**. Click it.
3. Check that:
   - The **base repository** is the original project.
   - The **base branch** is usually `main`.
   - The **head repository** is your fork.
   - The **compare branch** is `add-my-details`.
4. Give the PR a clear title:

   ```text
   Add my details to participant.md
   ```

5. Add a short description:

   ```text
   Adds my name and roll number to participant.md for GH-FOSS-T1.
   ```

6. Click **Create pull request**.

## 10. Wait for review

A maintainer will review your PR. If they ask for changes, edit the same branch, commit again, and push again—your PR will update automatically.

Once approved, they’ll merge your change into the original repository.
