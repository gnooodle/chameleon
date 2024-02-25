# chameleon (deprecated)
A private Firefox configuration

### Install

Make sure to set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true` in `about:config`, if it isn't already.

Add the `user.js` and `chrome/userChrome.css` to the directory of the Firefox profile in use.

Note: `chrome/userChrome.css` uses the Menlo font by default, not available on all systems, therefore a synonymous mono-spaced font is recommended.

### Recommendations

Extensions:
* Clickbait Remover for Youtube
* Dark Reader
* Decentraleyes
* Return YouTube Dislike
* uBlock Origin - My Filters:
```
! if using duckduckgo, removes annoying popup(s)
duckduckgo.com##.js-badge-main-msg.badge-link__wrap

! buffer fix, if still relevant
www.youtube.com##+js(nano-stb, resolve(1), 5000, 0.001)

! often annoying additions to the youtube homepage
www.youtube.com###foreground-content

!! youtube shorts !!

! Hide all videos containing the phrase "#shorts"
youtube.com##ytd-grid-video-renderer:has(#video-title:has-text(#shorts))
youtube.com##ytd-grid-video-renderer:has(#video-title:has-text(#Shorts))
youtube.com##ytd-grid-video-renderer:has(#video-title:has-text(#short))
youtube.com##ytd-grid-video-renderer:has(#video-title:has-text(#Short))

! Hide all videos with the shorts indicator on the thumbnail
youtube.com##ytd-grid-video-renderer:has([overlay-style="SHORTS"])
youtube.com##ytd-rich-item-renderer:has([overlay-style="SHORTS"])
youtube.com##ytd-video-renderer:has([overlay-style="SHORTS"])
youtube.com##ytd-item-section-renderer.ytd-section-list-renderer[page-subtype="subscriptions"]:has(ytd-video-renderer:has([overlay-style="SHORTS"]))

! Hide shorts button in sidebar
youtube.com##ytd-guide-entry-renderer:has-text(Shorts)
youtube.com##ytd-mini-guide-entry-renderer:has-text(Shorts)

! Hide shorts section on homepage
youtube.com##ytd-rich-section-renderer:has(#rich-shelf-header:has-text(Shorts))
youtube.com##ytd-reel-shelf-renderer:has(.ytd-reel-shelf-renderer:has-text(Shorts))

! Hide shorts tab on channel pages
! Old style
youtube.com##tp-yt-paper-tab:has(.tp-yt-paper-tab:has-text(Shorts))
! New style (2023-10)
youtube.com##yt-tab-shape:has-text(/^Shorts$/)

! Hide shorts in video descriptions
youtube.com##ytd-reel-shelf-renderer.ytd-structured-description-content-renderer:has-text("Shorts remixing this video")

! Remove empty spaces in grid
youtube.com##ytd-rich-grid-row,#contents.ytd-rich-grid-row:style(display: contents !important)
```
