# Argus · Where on Earth?

Pick a spot on the globe, grab a real astronaut photo from the ISS, and watch a vision pipeline work out exactly where it was taken. No GPS.

**Live demo:** https://prinks-wiz.github.io/argus-where-on-earth/

This is a replay of real outputs from a retrieve-then-match localizer built for the Argus spacecraft's vision-based orbit determination:

- **Retrieval:** DINOv2 + SALAD (LoRA fine-tuned) and FAISS
- **Matching:** SIFT + LightGlue
- **Georeferencing:** homography

Every similarity score, inlier count, correspondence, and error shown on the site comes from the pipeline run on a lab GPU.

Nothing is re-hosted here:

- Astronaut photos load live from [NASA GAPE](https://eol.jsc.nasa.gov/) (courtesy of the Earth Science and Remote Sensing Unit, NASA Johnson Space Center).
- Reference tiles are rebuilt from [Sentinel-2 cloudless 2021 by EOX](https://s2maps.eu) (CC BY-NC-SA 4.0).

Built by Priyanka Vijaybaskar.
