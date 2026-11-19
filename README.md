# Prediabetes explainer video (GitHub build)

Only 2 things are needed in the repo:
1. `build_video.py`  (repo root)
2. `.github/workflows/main.yml`

## Steps
1. New repo > Add file > **Upload files** > drag in `build_video.py` (just the file, not a folder) > Commit.
2. Add file > **Create new file** > name it exactly `.github/workflows/main.yml` > paste the workflow > Commit.
3. Settings > Actions > General > Workflow permissions > **Read and write** > Save.
4. Actions tab > **Build explainer video** > **Run workflow**. Takes ~10-20 min.
5. `prediabetes-explainer.mp4` appears in the repo root (also under the run's Artifacts).
6. Upload that mp4 to your calculator repo and paste `page-snippet.html` into your page.

## Voice
Uses Microsoft neural voices (Ava, Andrew, Emma "Multilingual", the most natural). The video is fitted to 2:00 automatically.
Fallbacks: Google voice, then captions + music only (the build never fails because of the voice).
For a fully human voice: record one file per scene and upload to a `voiceover/` folder next to build_video.py:
hook.mp3, what.mp3, silent.mp3, tests.mp3, calc.mp3, dpp.mp3, steps.mp3, outro.mp3

## Editing
Narration is the `NARRATION` list near the top of build_video.py. Screen ranges are `TESTS`, references are `REFS`.
Env options: TTS_VOICE, TTS_RATE (e.g. -5%), TARGET_SECONDS (default 120).
