# chameleon
A private Firefox configuration

### Install

Make sure to set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true` in `about:config`, if it isn't already.

Add the `user.js` and `chrome/userChrome.css` to the directory of the Firefox profile in use.

### Recommendations

Extensions:
* Clickbait Remover for Youtube
* Dark Reader
* Decentraleyes
* Return YouTube Dislike
* uBlock Origin - My Filters:
```
! buffer fix, if still relevant
www.youtube.com##+js(nano-stb, resolve(1), 5000, 0.001)

! if using duckduckgo, removes annoying popup(s)
duckduckgo.com##.js-badge-main-msg.badge-link__wrap

! often annoying additions to the youtube homepage
www.youtube.com###foreground-content
```
