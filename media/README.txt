cntrll. — media folder
=======================

Drop the files listed below into this folder using the EXACT filenames shown
(lowercase, hyphens, no spaces). The site will pick them up automatically —
no code changes required. Until a file exists, the matching placeholder
shows in its place.

Required files
--------------

  hero.mp4          Homepage hero background reel.
                    Used on: index.html (top of page).
                    Recommended: 10–20s silent loop, MP4 (H.264), 1920×1080,
                    target file size < 5 MB. No audio.

  live-hero.jpg     Live performance still.
                    Used on: index.html (chapter 01), live.html (page hero).
                    Recommended: high-res landscape JPG, ~2400×1350,
                    optimised to ~400 KB. Dark / moody works best with the
                    overlay.

  studio-hero.jpg   Studio still — kit, mics, control room.
                    Used on: index.html (chapter 02), studio.html (page hero).
                    Recommended: high-res landscape JPG, ~2400×1350,
                    optimised to ~400 KB.

  midi-hero.jpg     MIDI / piano-roll screenshot or texture.
                    Used on: index.html (chapter 03), midi.html (page hero).
                    Recommended: clean DAW screenshot or graphic abstraction,
                    landscape JPG/PNG, ~2400×1350.

  portrait.jpg      Professional portrait of cntrll.
                    Used on: about.html (asymmetric bio column).
                    Recommended: portrait orientation, 3:4 ratio
                    (e.g. 1200×1600), JPG, optimised to ~300 KB.


Optional / future
-----------------

You can later add: additional reel clips (live-reel-2.mp4 etc.), poster
images for video tags (hero-poster.jpg), social-share images, favicons.
None of these are required for the current pages to look complete.


Format notes
------------

  Video : .mp4 with H.264 + AAC, OR keep silent and drop audio entirely.
          Avoid .mov from a phone — re-encode to MP4 first
          (HandBrake / ffmpeg are both free).

  Images: .jpg for photographs, .png only if you need transparency.
          Compress before uploading — TinyPNG or Squoosh halve file size
          with no visible loss.


Replacing a placeholder with video instead of an image
------------------------------------------------------

Studio and MIDI currently use <img>. If you'd rather use a short video
loop in those slots, open the matching HTML file, find the line:

    <img src="media/studio-hero.jpg" alt="" onerror="this.remove();">

and replace it with:

    <video autoplay muted loop playsinline preload="metadata">
        <source src="media/studio-reel.mp4" type="video/mp4">
    </video>

Then drop a studio-reel.mp4 in this folder. Same pattern for midi.html.
