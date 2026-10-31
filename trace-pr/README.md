# TRACE pull request: the SOP detector inside the backend container

`0001-feat-sop-detector-run-the-SOP-detector-inside-the-ba.patch` is one commit for
[laxmi1707/PatternRecognSystem-Video2Text](https://github.com/laxmi1707/PatternRecognSystem-Video2Text),
made on top of its main at `6838018`. It runs the SOP detector inside the backend's container
on AWS, so merging it into main deploys it with the backend (`.github/workflows/deploy-backend.yml`)
and turns on the frontend's "Steps read from the video" panel. The commit message explains
each change. This branch only carries the patch; it changes nothing else in this repository.

To open the pull request, from a clone of the TRACE repository:

```bash
git checkout main && git pull
git checkout -b feat/sop-detector-in-backend
curl -fsSLO https://raw.githubusercontent.com/yoshualeo61-gif/SOP-detector/trace-sop-detector-patch/trace-pr/0001-feat-sop-detector-run-the-SOP-detector-inside-the-ba.patch
git am 0001-feat-sop-detector-run-the-SOP-detector-inside-the-ba.patch
git push -u origin feat/sop-detector-in-backend
```

Then open the pull request into main. Its "Build backend image" check builds and starts the
image (about 20-30 minutes) before anything is merged.
