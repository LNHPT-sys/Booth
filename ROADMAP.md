# BOOTH roadmap

BOOTH is a phone-first vocal booth: load a beat, record over it, stack takes, export.
`index.html` is the whole app.

## Up next: full UI overhaul

The overhaul is planned for last, but every new feature should be built so it
fits it. Rules taken from real use:

- **Plain words, no studio jargon.** "Mute" and "Solo", never "M" and "S". If a
  control needs explaining, rename it or show what it does.
- **Touch it directly.** Drag clips to move them and drag the timeline to scrub.
  Buttons are shortcuts, never the only way to do something.
- **Everything can be undone.** Any edit pushes an undo step first, including
  moves, deletes, clears and sync locks. Nothing destructive happens without
  undo or a confirm.
- **No surprises.** An accidental tap must never move or change audio in a way
  you can't see and reverse.
- **Record-first layout.** Keep the controls you need while recording in reach
  without scrolling; push setup and diagnostics out of the way.
- **Mobile only.** Everyone records on a phone with headphones. No features
  that assume a speaker, studio monitors or a live room (Align, bleed removal
  and the vocal processing were removed for this reason).
- **Your data stays on your phone.** Sessions are saved in each person's own
  browser and are never shared through the link.

## Done

- Bluetooth latency lock-in keeps its correction when a take starts at 0:00
- Sessions: new, open, rename, clear, delete
- Live volume, pan, mute and solo during playback; sync restarts in place
- Finger scrubbing on the transport bar and every lane
- Drag takes to move them; undo for every edit (button and Ctrl/Cmd+Z)
- Align removed; the beat's tempo is now measured on load so the Bar buttons
  always work
- Raw audio only: the vocal processing was removed after it made takes sound
  worse; recording asks for 256kbps

## Ideas, not started

- Trim the start and end of a take, split, cut out a section
- Punch in: re-record one bar or line
- Zoom the timeline; loop a section such as the hook
- Markers for verse and hook
