# splitgravity.com

The site for **Split Gravity**, served by GitHub Pages from the repository root.

```
index.html          landing page
privacy-policy.html required by the App Store and by AdMob
app-ads.txt         must stay at the root — ad exchanges look for it there
assets/             icon exports and one screenshot
CNAME               custom domain
```

## Two rules

**`app-ads.txt` lives at the root.** `splitgravity.com/app-ads.txt`, never inside a
folder. It is what stops someone spoofing the bundle ID and selling fake impressions
against the app's name. AdMob re-crawls it roughly every 24 hours.

**Do not change the domain after launch.** AdMob looks for `app-ads.txt` at the root of
whatever marketing URL the App Store listing carries. Move the domain and verification
resets.

## The hero is not an image

The arena at the top of the page is built from CSS — lanes, scrolling grid, beam, orbs
and gates. That is deliberate. Screenshots go stale every time the interface changes,
and the game itself ships with no image assets either: everything is generated at
runtime. The palette here uses the same hex values as `Theme.swift`.

Only two real images are used: the app icon, and one capture of the game-over screen.

## When the app is live

1. Replace the disabled "Coming to the App Store" button in `index.html` with the real
   store link.
2. Add fresh screenshots to `assets/` if you want a gallery — take them from a current
   build, not from an old one.
