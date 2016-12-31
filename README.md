# Meaty-M

> Easily post articles to Medium.


## Dependencies

- [jq](https://stedolan.github.io/jq) - Used to parse JSON responses.


## Install

```
$ curl https://raw.githubusercontent.com/kjbrum/meaty-m/master/meaty-m > ~/bin/meaty-m
$ chmod +x ~/bin/meaty-m
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
    --license=<string>          The license of the post (all-rights-reserved|cc-40-by|public-domain|...)
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

    More information at https://github.com/Medium/medium-api-docs#creating-a-post

Examples:
    $ meaty-m --content=new-post.md --title="How to Post a Cool Post" --tags='["dopesauce","awesome"]' --status=draft
    $ meaty-m --content=new-post-2.md --title="Just Another Cool Post" --format=html --notify
```


## Config

##### MEATY_M_TOKEN

Your Medium integration token. [Find here under "Integration tokens"](https://medium.com/me/settings)

##### MEATY_M_SECRET

Your Medium author ID. Run `meaty-m --user` after installing the script and adding your token.


## License

Copyright © [Kyle Brumm](http://kylebrumm.com). Free to use on whatever and may be redistributed under the terms specified in the [license](LICENSE.md).
