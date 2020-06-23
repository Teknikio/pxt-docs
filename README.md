You can find the original README.md info for the microbit-pxt from which this repo is forked at ORIGINAL_REPO_README.md [Original Readme](ORIGINAL_REPO_README.md)

# Working on the Teknikio Documentation

- Make sure to checkout a new branch before editing:

```
git checkout -b YOUR_NAME/WHAT_YOURE_DOING
```

- Install dependencies

```
npm install
```

- Run local develpoment server

```
pxt serve
```

- Visit localhost:3232/docs

- To find the markdown file you need to edit, navigate using the main website, to for example:
  https://docs.teknikio.com/docs/blocks/on-start.html

To edit this page, you need to edit the corresponding Markdown file, it will have the same name as the last portion of the url, but will end in `.md` instead of `.html`. So to edit this page I would need to edit `on-start.md`

- Edit a Markdown file `.md`. You can use a code editor like VSCode to view a preview as you edit the file.

- Once your edits are complete, open a pull request to master. After it's been merged, follow the steps below to deploy new changes.

# How to deploy new changes

- Once the changes are ready, run

```
pxt staticpkg
```

- Copy the generated files from `/built/packaged/docs` to the S3 bucket `docs.teknikio.com`

- Avoid copying the full folder as this takes a very long time to upload to S3, and try to retrieve only the relevant files from the built output.

- CloudFront will cache the files for 24 hours, if you need to see your changes reflected immediately, you can visit the CloudFront distribution for AWS and invalidate the files:
  https://console.aws.amazon.com/cloudfront/home#distribution-settings:E2LNR9UBUJNBSX
