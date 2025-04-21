# v1-archive

This is a repository which attempts to preserve a static version of the first iteration of Audioxide which was a Wordpress blog with a custom theme. Prior to being removed entirely, it was last hosted at https://audioxide.github.io/v1-archive until April 2025, when it was removed from the public internet.

[View the archived version](https://audioxide.github.io/v1-archive)

## Method of preservation

### Site crawl

The following command was run to produce the initial static files:

```bash
wget -m -k -K -E http://old.audioxide.com --no-check-certificate
```

This command uses the `wget` command to create a local copy of the website:
- `-m`: Mirror mode, recursively downloads all linked content
- `-k`: Converts links to make them suitable for local viewing
- `-K`: Keeps original file timestamps when converting
- `-E`: Appends .html extension to appropriate files
- `http://old.audioxide.com`: The URL to crawl
- `--no-check-certificate`: Skips SSL certificate validation, as the SSL certificate was never valid for the old.audioxide subdomain

### Domain corrections and amendments

A range of find-and-replace corrections have been made to the original crawl.

- https://audioxide.github.io/v1-archive has been used for assets and links
- https://audioxide.com has been used for sharing and canonical links in case they're picked up by search engines (where we want to direct users to the live site)