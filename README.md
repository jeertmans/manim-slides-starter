# Manim Slides Starter

[![Deploy static content to Pages](../../actions/workflows/deploy_pages.yml/badge.svg)](../../actions/workflows/deploy_pages.yml)

Starter template for Manim Slides presentations and GitHub Pages deployment!

## Who is this template for?

This template is for people that would like to share their Manim Slides
presentation with others, anywhere on the internet.

## How to use this template?

This template contains two important files:

+ [`slides.py`](./slides.py);
+ and [`deploy_pages.yml`](./.github/workflows/deploy_pages.yml);

The former contains the logic to animate your slides, while the
second defines a number of steps to render your slides into a
portable presentation format, and publish it on the internet.
It uses [GitHub actions](https://github.com/features/actions)
and
[GitHub pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
which are free for public repositories.

### Creating a new repository

First, you need to create a new repository by clicking on the
[*Use this template*](https://github.com/new?template_name=manim-slides-starter&template_owner=jeertmans)
button.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jeertmans/manim-slides-starter/assets/27275099/dabb51b9-77f1-45e7-833b-d53c8af0a7d0">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/jeertmans/manim-slides-starter/assets/27275099/75045605-fce0-46d0-98e0-8a85cec907cb">
    <img width="65%" alt="Creating a new repository from this template" src="https://github.com/jeertmans/manim-slides-starter/assets/27275099/75045605-fce0-46d0-98e0-8a85cec907cb">
  </picture>
</p>

> NOTE: if you want to have a private repository, you will probably need
  a GitHub Pro account.

### Customizing your presentation

By default, the generated presentation is obtained from the
[`slides.py`](./slides.py) file, uses Manim Community Edition,
and renders the following scenes: `Introduction`, `WithTeX`,
ans `Outro`.

Of course, you can update or create Python files to
generate your animations. If you require a specific
version of `manim-slides`, `manim` or `manimlib`,
please edit [`requirements.txt`](./requirements.txt).

Additionally, you can edit the following environ variables
to reflect your changes:

https://github.com/jeertmans/manim-slides-starter/blob/d9799748b124c71626175de8d156c8010bf6f68d/.github/workflows/deploy_pages.yml#L19-L23

> **WARNING**: `manimgl` is currently not supported, as rendering animations
> inside GitHub workflows seems complex...

Last, if you want to change the scenes rendering and the HTML
conversion, feel free to edit the last two lines:

https://github.com/jeertmans/manim-slides-starter/blob/d9799748b124c71626175de8d156c8010bf6f68d/.github/workflows/deploy_pages.yml#L93-L96

## Where is the output?

On every commit to the `main` branch, a new deployment action should be
triggered. If that is not the case, inspect the [actions](../../actions) tab for
any error message. You can also manually trigger a deployment by clicking on
the [*Run workflow*](../../actions/workflows/deploy_pages.yml) button.

If everything goes well, the deploying site should be on your
personal GitHub pages site: `https://<username>.github.io/<repository_name>`.

For example, this starter's website is:
https://jeertmans.github.io/manim-slides-starter.

> NOTE: the first time the deployment action is used,
> the `gh-pages` branch is created. You might need
> to go to [`Settings -> Pages`](../../settings/pages)
> and make sure that the *Source* is
> *Deploy from a branch*, and *branch* is *gh-pages*.
