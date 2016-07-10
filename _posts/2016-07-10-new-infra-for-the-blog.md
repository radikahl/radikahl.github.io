---
layout: post
title: New Infra for the Blog
excerpt_separator: “”
---
After using [Schnitzelpress](https://github.com/hmans/schnitzelpress) and a self-build hack for a long time I switched platforms again: [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) hosted on Github.

Of course, I handcrafted it to my needs:

* More control over the post teasers (aka excerpts). By re-activating the [*excerpt_separator*](https://jekyllrb.com/docs/posts/#post-excerpts) YAML parameter I can precisely define how how long the excerpt should be. ([relevant commit](https://github.com/radikahl/radikahl.github.io/commit/7beb5b95f996adb295ba910bd817340f07fecbad))
* Hide the post title. I added a *hide-title* YAML parameter to be able to hide a post title when requested. This improves, IMHO, the aesthetics of the photo-only posts. ([relevant commit](https://github.com/radikahl/radikahl.github.io/commit/cb6dd7ab264201fc2a92a3e3dbc51217bea4997c))
* Added Responsive Youtube embeds. Now embedded YouTube videos look great on desktop machines and mobile devices. ([relevant commit](https://github.com/radikahl/radikahl.github.io/commit/e8f2c7aef1c3a2ef726e738ab2895ddb6d56a24d) & [example post](https://github.com/radikahl/radikahl.github.io/commit/28b8b3f265407adb15e6841fa24ba0fe15efdd7d#diff-4bb7c44b0f38c19b6624845eae60106a))
