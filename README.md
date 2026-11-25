# Moushumi Pervin — Academic Website

A Quarto academic website with automatic publishing to GitHub Pages.

## First-time setup in your browser

1. Sign in to your GitHub account.
2. Create a PUBLIC repository named YOURUSERNAME.github.io. Replace YOURUSERNAME with your exact GitHub username. For example, if your username is moushumipervin, use moushumipervin.github.io.
3. Initialize the repository with a README if GitHub offers that option.
4. Open the repository, choose Add file > Upload files, and upload all the CONTENTS of this extracted folder. Do not upload the ZIP or the enclosing folder itself. Keep the assets and .github folders intact.
5. Commit the uploaded files to the main branch.
6. Open Settings > Pages. Under Build and deployment > Source, select GitHub Actions.
7. Open the Actions tab. Open Publish academic website. If the first run failed because Pages was not enabled yet, choose Re-run all jobs. You can also choose Run workflow to start a new run.
8. Wait until build and deploy both show green checks. Settings > Pages will display your live site URL.

The workflow must appear at .github/workflows/publish.yml. It will not work if uploaded as a plain publish.yml at the repository root.

## How to edit your website

Open a source file in GitHub and click the pencil icon (Edit this file). Change the text, preserve the surrounding HTML tags, and click Commit changes. GitHub Actions will rebuild and publish the site automatically.

| File | Content |
| --- | --- |
| index.qmd | Homepage introduction, research highlights, and contact links |
| research.qmd | Research descriptions |
| publications.qmd | Papers and publication statuses |
| teaching.qmd | Courses and mentoring |
| cv.qmd | CV overview |
| styles.css | Colors, fonts, spacing, and responsive design |
| _quarto.yml | Navigation, title, footer, and output folder |
| assets/Moushumi_Pervin_CV.pdf | Downloadable CV; replace with the same filename |

These Quarto pages use HTML inside a raw HTML block. For a simple text edit, change the words between tags such as <p> and </p>, keeping the tags and the opening/closing triple-backtick lines.

You do not need to edit the generated HTML. The dist directory is created automatically during publication and is excluded from Git.

## Optional local preview

Install Quarto from https://quarto.org/docs/get-started/ and run `quarto preview` in this folder. Run `quarto render` to generate the finished site in dist/.

## References

- https://quarto.org/docs/publishing/github-pages.html
- https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages
