# Meaty-M

> Easily post articles to Medium.


## Dependencies

- [jq](https://stedolan.github.io/jq) - Used to parse JSON responses.


## Install

```
$ curl https://raw.githubusercontent.com/kjbrum/kraken-cli/master/kraken > ~/bin/kraken
$ chmod +x ~/bin/kraken
```


## Usage

```
Meaty-M

Easily post articles to Medium.

Usage:
    $ meaty-m <options>

Options:
    --content=<path/to/file>    The body of the post, in a valid, semantic, HTML fragment, or Markdown (required)
    --format=<string>           The format of the "content" field (markdown|html) (required)
    --help                      Display the help text
    --license=<string>          The license of the post (all-rights-reserved|cc-40-by|cc-40-by-sa|cc-40-by-nd|cc-40-by-nc|cc-40-by-nc-nd|cc-40-by-nc-sa|cc-40-zero|public-domain)
    --notify                    Whether to notify followers that the post was published
    --status=<string>           The status of the post (public|draft|unlisted)
    --tags=<string|array>       Tags to classify the post
                                    - Only the first three will be used
                                    - Tags longer than 25 characters will be ignored
    --title=<string>            The title of the post (required)
                                    - Used for SEO and when rendering the post as a listing
                                    - Titles longer than 100 characters will be ignored
    --url=<url>                 The original home of this content, if it was originally published elsewhere
    --user                      Display your author ID

    More information. (https://github.com/Medium/medium-api-docs#creating-a-post)

Example:
    $ meaty-m
```


## Config

[Find/create your API credentials here.](https://kraken.io/account/api-credentials)

##### MEATY_M_KEY

Your Medium API key.

##### MEATY_M_SECRET

Your Medium API secret.


## License

Copyright © [Kyle Brumm](http://kylebrumm.com). Free to use on whatever and may be redistributed under the terms specified in the [license](LICENSE.md).
