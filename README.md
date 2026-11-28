# Virtual Pipe Organ

A free browser pipe organ laid out as a real console: two stop jambs with 240+ drawknobs between them, 5 manuals with thumb pistons, expression shoes, a crescendo pedal, toe studs and a 32-note pedalboard. It also has couplers, tremulants, 8 piston memory levels, rooms, temperaments, WAV recording, Web MIDI and a hymn trainer.

**Play:** https://virtualpipeorgan.github.io/organ/

Single file (`index.html`), no dependencies. MIDI has three modes, set in Settings:
- **By channel:** ch1 Pedal, ch2 Choir, ch3 Great, ch4 Swell, ch5 Solo, ch6 Echo.
- **One keyboard:** any channel plays the selected manual.
- **Split:** below middle C plays the pedal.

Controllers: CC11 expression, CC64 sustain, CC7 volume, CC123 all notes off (that channel only); program change 0–9 selects generals.

## Hymn trainer
Pick a hymn on the music desk:
- **Listen:** the organ plays the melody on the Great.
- **Learn:** each note falls onto its key and waits for you.
- **Play:** notes keep time and are scored Perfect, Good or Miss, with a streak counter, 1–3 stars and a saved best score.

You can play the tunes on any manual or on MIDI. On phones the keyboard follows the melody, and all manuals slide together from the grip rail.

The melodies are public-domain tunes taken from the MusicXML scores on [Hymnary.org](https://hymnary.org/) and the ABC scores of the [Open Hymnal](https://openhymnal.org/), each of which states that it is public domain. Only the melody is used, not any hymnal's harmonisation.

## Pro and payments (owner)
- Pro is sold through Stripe Payment Links, with Stripe as merchant of record. The products are Pro at US$12 once, Pro at US$3 a month, and a church licence at US$39.
- The links live in the `SHOP` block at the start of the UI script. Stripe's confirmation page shows the unlock code.
- `codes` holds SHA-256 hashes of the unlock codes. Rotate the code each major release, and keep the old hashes so earlier buyers stay unlocked.
- Pro adds piston memory levels 2–8 and saving/loading registration files. Recording and everything else stay free.

Unlocking happens in the browser, and the source is public, so it works on the honour system.

`?reset` in the URL clears saved settings.
