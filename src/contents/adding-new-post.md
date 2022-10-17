---
author: Sat Naing
datetime: 2022-09-23T15:22:00Z
title: Adding new posts in AstroPaper theme
slug: adding-new-posts-in-astropaper-theme
featured: true
draft: false
tags:
  - docs
ogImage: ""
description:
  Some rules & recommendations for creating or adding new posts using AstroPaper
  theme.
---

Here are some rules/recommendations, tips & ticks for creating new posts in AstroPaper blog theme.

## Table of contents

## Frontmatter

Frontmatter is the main place to store some important information about the post (article). Frontmatter lies at the top of the article and is written in YAML format. Read more about frontmatter and its usage in [astro documentation](https://docs.astro.build/en/guides/markdown-content/).

Here is the list of frontmatter property for each post.

| Property          | Description                                                                               | Remark                    |
| ----------------- | ----------------------------------------------------------------------------------------- | ------------------------- |
| **_title_**       | Title of the post. (h1)                                                                   | required<sup>\*</sup>     |
| **_description_** | Description of the post. Used in post excerpt and site description of the post.           | default = SITE.desc       |
| **_author_**      | Author of the post.                                                                       | default = SITE.author     |
| **_datetime_**    | Published datetime in ISO 8601 format.                                                    |                           |
| **_slug_**        | Slug for the post. Usually the all lowercase title seperated in `-` instead of whtiespace | default = slugified title |
| **_featured_**    | Whether or not display this post in featured section of home page                         | default = false           |
| **_draft_**       | Mark this post 'unpublished'.                                                             | default = false           |
| **_tags_**        | Related keywords for this post. Written in array yaml format.                             |                           |
| **_ogImage_**     | OG image of the post. Useful for social media sharing and SEO.                            | default = SITE.ogImage    |

`title` and `slug` fields in frontmatter must be specified.

Title is the title of the post and it is very important for search engine optimization (SEO).

`slug` is the unique identifier of the url. Thus, `slug` must be unique and different from other posts. The whitespace of `slug` needs to be separated with `-` or `_` but `-` is recommended. If slug is not specified, the slugified title of the post will be used as slug.

Here is the sample frontmatter for the post.

```yaml
# src/contents/sample-post.md
---
title: The title of the post
author: your name
datetime: 2022-09-21T05:17:19Z
slug: the-title-of-the-post
featured: true
draft: false
tags:
  - some
  - example
  - tags
ogImage: ""
description: This is the example description of the example post.
---
```

## Adding table of contents

By default, a post (article) does not include any table of contents (toc). To include toc, you have to specify it in a specific way.

Write `Table of contents` in h2 format (## in markdown) and place it where you want it to be appeared on the post.

For instance, if you want to place your table of contents just under the intro paragraph (like I usually do), you can do that in the following way.

```md
---
# some frontmatter
---

Here are some recommendations, tips & ticks for creating new posts in AstroPaper blog theme.

## Table of contents

<!-- the rest of the post -->
```

## Headings

There's one thing to note about headings. The AstroPaper blog posts use title (title in the frontmatter) as the main heading of the post. Therefore, the rest of the heading in the post should be using h2 \~ h6.

This rule is not mandatory, but highly recommended for visual and SEO purposes.

## Bonus

### Image compression

When you put images in the blog post, it is recommended that the image is compressed. This will affect the overall performance of the website.

My recommendation for image compression sites.

- [TinyPng](https://tinypng.com/)
- [TinyJPG](https://tinyjpg.com/)

### OG Image

The default OG image will be placed if a post does not specify the OG image. Though not required, OG image related to the post should be specify in the frontmatter. The recommended size for OG image is **_1200 X 640_** px.

CNN  —  none
The Trump Organization charged the Secret Service “exorbitant rates” – upwards of $1.4 million over four years – to protect the former President and his family at properties they owned, according to documents released by the House Oversight Committee on Monday.

The committee found that the Trump Organization charged the Secret Service “excessive nightly rates on dozens of trips” as high as $1,185 per night despite claims by the former President’s company that federal employees traveling with him would stay at those properties “for free” or “at cost.”

“The exorbitant rates charged to the Secret Service and agents’ frequent stays at Trump-owned properties raise significant concerns about the former President’s self-dealing and may have resulted in a taxpayer-funded windfall for former President Trump’s struggling businesses,” the panel’s chairwoman, New York Democratic Rep. Carolyn Maloney, wrote in a letter to the service’s director on Monday.

When he was president, Trump traveled frequently to properties his company ran as businesses, including Mar-a-Lago in Palm Beach, Florida, and the Trump National Golf Club in Bedminster, New Jersey. While he was there, some agents and officers stayed in rooms at those properties, though others rented rooms at nearby hotels.

Charging his protective detail for lodging at his own properties was a controversial practice when Trump was in office and has continued in his post-presidency.

Maloney also notes that her committee has been seeking a full accounting of the Secret Service’s expenditures at Trump-owned properties for more than two years but still has not received complete information on nightly rates or the total amount the agency spent, which “appears to exceed $1.4 million of taxpayer money.”

The committee is still seeking records from the Secret Service, noting the panel is looking at potential legislation to prevent “presidential self-dealing and profiteering, as well as to curb conflicts of interest by ensuring that future presidents are prevented from exercising undue influence on Secret Service spending.”

Representatives for the Trump Organization could not immediately be reached for comment.

CNN also has reached out to the Secret Service for comment.

The committee said the Trump Organization charged the Secret Service more than the government rate at least 40 times from January 2017 to September 2021.

One of those times was in March 2017 when the Trump Organization charged a nightly rate of $1,160 to stay at the Trump hotel in Washington, DC, to protect Eric Trump, who was promoting a golf tournament at the Trump National Golf Club. According to the General Services Administration’s website, the per diem rate was $242 in March 2017 in Washington, DC.

CNN’s Kevin Liptak contributed to this report.
