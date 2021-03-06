# hugo-theme-mfw

Minimal [Hugo](https://gohugo.io/) theme inspired by [Motherfucking Website](http://motherfuckingwebsite.com/) and its descendants, as well as Jeremy Thomas' [Web Design in 4 Minutes](https://jgthms.com/web-design-in-4-minutes/)

## Installation

## Development

## Configuration

```toml
# this theme places the meta generator tag at a better position in <head> manually
disableHugoGeneratorInject = true
```

## Before First Release

TODO: comb over every html element/attribute for semantic appropriateness
TODO: add lots of configuration hooks via config.toml and overriding templates
TODO: check all generated pages for weird unreachable leafs or duplicated content that should be meta refreshed away
TODO: decide on yaml vs toml for front matter
TODO: show permalinks.post example config
TODO: extra in header (prepend and append before/after links) footer partials and blocks for subtemplates
TODO: translation function call on all static text
TODO: ship with an exampleSite, include showcase demo page of all html elements:
  <https://github.com/Pewpewarrows/MyModernLife/blob/master/src/templates/demo.html>
  <https://github.com/cbracco/html5-test-page>
TODO: images/{screenshot,tn}.png for being featured on hugoThemes
TODO: front matter showDate default false, blog posts true
TODO: front matter cover image (abs path by default, useRelativeCover option as well)
TODO: a lot of themes have {{ .Title | markdownify }} as well as for Description, Summary? but then {{ .Summary | plainify }} in meta tags
TODO: might need this trick at some point for determining content types:
  {{ $isntDefault := not (or (eq (trim $.Site.Params.contentTypeName " ") "posts") (eq (trim $.Site.Params.contentTypeName " ") "")) }}
  {{ $contentTypeName := cond $isntDefault (string $.Site.Params.contentTypeName) "posts" }}
TODO: closing comments for all html ids or significant classes with large blocks inside
TODO: update hugo to latest, taxonomy and taxonomyTerm are now term and taxonomy, respectively
TODO: hugo modules? especially for js build systems?
TODO: customized simple versions of social shortcodes (insta, twitter, etc)
TODO: as part of i18n will want to use that template tag for all static text (like "minute read")

- [ ] .Site.Params.title is used in opengraph template instead of .Site.Title
- [ ] evaluate generated html for whitespace to remove with {{- -}}
- [ ] improved default RSS template with images <https://github.com/brunoamaral/future-imperfect-DI/blob/master/layouts/_default/rss.xml>

## Github Issues

TODO: shortcodes for info/warning boxes
TODO: offer analytics optional
TODO: offer comments optional, have comment = true in blog front matter, default to false, offer multiple comment engines or overridable partial
TODO: on build, pull from analytics data file, edit rating or viewcount front matter on each content page, allows for somewhat dynamic popular listings?
TODO: optional share menu
TODO: formspree.io for contact forms?
TODO: USERS.md git list?
TODO: buymeacoffee.com sponsorship, patreon, others?
TODO: img, figure (maybe, if better than built-in), imgproc shortcodes: <https://github.com/panr/hugo-theme-hello-friend/tree/master/layouts/shortcodes> <https://gohugo.io/content-management/image-processing/#image-processing-examples>
TODO: github bots: dependabot, others? <https://probot.github.io/apps/> <https://dev.to/pierre/automation--use-githubs-bots-to-increase-your-productivity--30j5>
TODO: render TOC as an ol instead of ul
TODO: placeholder shortcode templates for rest of embeds that require external API calls during build

- [ ] add schema.org and JSON-LD metadata to head and individual elements
  - <https://github.com/brunoamaral/future-imperfect-DI/blob/master/layouts/_default/baseof.html>
- [ ] equivalent to django-debug-toolbar (see <https://github.com/JugglerX/hugo-debug-bar> for prototype), showing printf of all variables on the page, including Hugo ones, build.writeStats file reading
  - <https://github.com/zwbetz-gh/starter-hugo-debug-site/blob/master/layouts/partials/debug-table.html>
  - <https://github.com/kaushalmodi/hugo-debugprint>
  - <https://github.com/danielfdickinson/hugoDebugTables>
  - <https://discourse.gohugo.io/t/easier-debugging-hugo-variables-using-the-javascript-console/22873>
- [ ] automated scanner/linter to ensure that ref is used instead of relref in syndicated content (allows links to be clicked when read from feed reader), also ensure images are absolute URLs too
- [ ] adjustable page size would require pre-rendering lots of various options, but might be worth exploring

## Place in Other Themes

TODO: offer optional [live chat tools](https://www.sideprojectchecklist.com/2017/customer-chat-tools/)
