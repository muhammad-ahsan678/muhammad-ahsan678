# Setup Guide

## What updates automatically

- **Followers badge:** updates when your follower count changes.
- **Profile views:** increments as the profile is viewed.
- **Repository cards:** update descriptions, languages, stars, and forks.
- **GitHub statistics:** refresh from your public GitHub activity.
- **Top languages:** recalculates from your public repositories.
- **Contribution streak:** refreshes automatically.
- **Contribution snake:** regenerated daily by GitHub Actions.

The text sections, skills list, learning goals, and featured repository choices remain manual because GitHub cannot accurately infer your intentions.

## Installation through GitHub website

1. Create a **public** repository named exactly:

   `muhammad-ahsan678`

2. Upload the contents of this package while preserving this structure:

```text
muhammad-ahsan678/
├── README.md
└── .github/
    └── workflows/
        └── snake.yml
```

3. Commit the files to the repository's `main` branch.

4. Open the repository's **Actions** tab.

5. Select **Generate contribution snake**.

6. Click **Run workflow** and run it once.

7. Wait for the workflow to finish, then refresh your GitHub profile.

## Required Actions permission

The workflow normally works with the permission declared inside `snake.yml`.

If publishing fails with a permission error:

1. Open the profile repository.
2. Go to **Settings → Actions → General**.
3. Under **Workflow permissions**, choose **Read and write permissions**.
4. Save and run the workflow again.

## Installation using Git

```bash
git clone https://github.com/muhammad-ahsan678/muhammad-ahsan678.git
cd muhammad-ahsan678
```

Copy `README.md` and the `.github` directory into the cloned repository, then run:

```bash
git add README.md .github/workflows/snake.yml
git commit -m "Add automated GitHub profile README"
git push origin main
```

## Troubleshooting

### Snake image is blank or broken

Run the workflow manually from the **Actions** tab. The `output` branch and SVG files do not exist until the first successful run.

### Statistics temporarily fail to load

External statistics cards can occasionally be rate-limited or unavailable. They generally recover automatically; no repository change is required.

### Profile README does not appear

Confirm all three conditions:

- Repository name is exactly `muhammad-ahsan678`
- Repository is public
- `README.md` is in the repository root

## Optional personalization

Replace or add repository cards using:

```html
<a href="https://github.com/muhammad-ahsan678/REPOSITORY">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=muhammad-ahsan678&repo=REPOSITORY&hide_border=true">
</a>
```

Change both occurrences of `REPOSITORY` to the exact repository name.
