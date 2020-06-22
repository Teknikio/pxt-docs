You can find the original README.md info for the microbit-pxt from which this repo is forked at ORIGINAL_REPO_README.md [Original Readme](ORIGINAL_REPO_README.md)

# Working on the Teknikio Documentation

- Install dependencies

```
npm install
```

- Run local develpoment server

```
pxt serve
```

- Visit localhost:3232/docs

- Edit a Markdown file `.md`. You can use a code editor like VSCode to view a preview as you edit the file.

- Once the changes are ready, run

```
pxt staticpkg
```

- Copy the generated files from `/built/packaged/docs` to the S3 bucket `docs.teknikio.com`

- Avoid copying the full folder as this takes a very long time to upload to S3, and try to retrieve only the relevant files from the built output.

- CloudFront will cache the files for 24 hours, if you need to see your changes reflected immediately, you can visit the CloudFront distribution for AWS and invalidate the files:
  https://console.aws.amazon.com/cloudfront/home#distribution-settings:E2LNR9UBUJNBSX
