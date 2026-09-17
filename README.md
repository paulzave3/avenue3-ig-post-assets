# Avenue3 Studios — Instagram post assets

Public image staging for the [Avenue3 Studios Instagram automation
pipeline](https://github.com/paulzave3/avenue3-instagram-automation) (that repo is
private; this one exists only because it has to be public).

## Why this repo is public

Buffer's post-creation API requires a real, internet-reachable URL for every image —
there's no upload endpoint and no way to hand it a local file. This repo exists purely
to give each rendered or selected post image a public URL Buffer can fetch, using
GitHub's raw-content URLs (`https://raw.githubusercontent.com/paulzave3/avenue3-ig-post-assets/main/<path>`).

Every image here is either about to become, or already is, a public Instagram post —
being briefly (or permanently) visible here isn't a new exposure.

## What's NOT here

No unrelated business files, no draft captions, no anything that isn't the final
image for a specific post. The automation pipeline's actual logic, config, and
internal docs live in the private `avenue3-instagram-automation` repo, not here.

## Convention

`posts/<YYYY-MM-DD>-<format>.jpg` — one file per post, kept permanently (not deleted
after use). Two reasons to keep rather than clean up:

1. Buffer creates drafts with `saveToDraft: true`, and a draft can sit in the queue
   for a while before Paul approves and publishes it — the image needs to stay
   reachable at that URL for as long as the draft exists, not just at creation time.
2. Nothing in a git repo is ever really temporary anyway (an old file's content stays
   fetchable via its commit history even after being removed from the current tree),
   so keeping a clean, permanent, dated archive is more useful than pretending
   otherwise.
