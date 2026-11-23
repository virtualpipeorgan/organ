# Virtual Pipe Organ

A free browser pipe organ laid out as a real console: two stop jambs with 240+ drawknobs between them, 5 manuals with thumb pistons, expression shoes, a crescendo pedal, toe studs and a 32-note pedalboard. It also has couplers, tremulants, 8 piston memory levels, rooms, temperaments and Web MIDI.

**Play:** https://virtualpipeorgan.github.io/organ/

Single file (`index.html`), no dependencies. MIDI has three modes, set in Settings:
- **By channel:** ch1 Pedal, ch2 Choir, ch3 Great, ch4 Swell, ch5 Solo, ch6 Echo.
- **One keyboard:** any channel plays the selected manual.
- **Split:** below middle C plays the pedal.

Controllers: CC11 expression, CC64 sustain, CC7 volume, CC123 all notes off (that channel only); program change 0–9 selects generals.

## Monetising (owner)
Edit the `SHOP` block near the start of the UI script in `index.html`:
- `support`: a donation link (Ko-fi, Buy Me a Coffee, GitHub Sponsors, PayPal.me). It shows a ♥ Support button.
- `buy`: the Lemon Squeezy (or Gumroad) checkout for Pro, priced at US$12 once. Until `buy` is set, Pro features stay unlocked for everyone.
- `site`: an optional second checkout for a church/site licence, priced at US$39. It uses the same code.
- Put the unlock code in each product's receipt or thank-you text, so it is delivered automatically.
- `codes`: SHA-256 hashes of the unlock codes. The first one is already in. Rotate the code each major release and keep the old hashes, so earlier buyers stay unlocked. Hash a code with
  `node -e "console.log(require('crypto').createHash('sha256').update('YOUR-CODE').digest('hex'))"`.
  With an empty list, any code of 6 or more characters unlocks.

Pro adds WAV recording, piston memory levels 2–8, and saving/loading registration files. Everything else stays free.

Unlocking happens in the browser, and the source is public, so it works on the honour system.

`?reset` in the URL clears saved settings.
