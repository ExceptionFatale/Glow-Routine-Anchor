# HITCHHIKERS — Game State Document
# Maintained by the Hitchhiker Synthesizer skill.
# Load this at the start of every session. It replaces piecing together after-actions.
# Last synthesized: SESSION Aug 20 2026 (log line ~13040)

---

## 🎯 CURRENT STATE

**Restore file:** `HITCH_HATCH.qzl`
**Location on restore:** Hatchway (bottom of gangway)
**Score:** 28 / 400
**Move:** ~695
**To reach Intelligence Door from restore:** up → port (2 moves)
**To reach Engine Room from restore:** up → aft (2 moves)

**Current inventory (as of Aug 20 session):**
- no tea *(specific dismissal)*
- Advanced Tea Substitute *(yawn)*
- sales brochure *(specific dismissal)*
- Sub-Etha signaling device *(yawn)*
- thing from aunt (Made in Ibiza) *(yawn)*
- The Hitchhiker's Guide *(specific dismissal)*
- toothbrush *(yawn)*
- tweezers *(specific dismissal when Marvin present; yawn when absent)*
- molecular hyperwave pincer *(yawn)*

**NOT in inventory — notable items:**
- Spare Improbability Drive: dropped in Engine Room at move 679 *(specific dismissal at door)*
- Flathead screwdriver: status unclear after Aug 18 session — check Engine Room or Galley
- Strange gun: on the Bridge
- Satchel: on the Bridge
- Handbag: on the Bridge
- Sales brochure: in inventory (confirmed Aug 20)

**⚠️ Score anomaly:** Score dropped from 33 → 3 somewhere between moves 312 and 381. Cause not identified. Possibly drinking the ATS or doing something wrong on the ship. A subsequent death brought score to -2 per Aug 18 after-action (ATS death). Current score is 28 so the game was restored after deaths. **The gap between move 312 and 381 in the log is unread — this should be reviewed.**

---

## ✅ SOLVED SEQUENCES (never revisit)

**Bedroom escape** (~9 chained moves from dark):
`turn on light → get up → take gown → wear gown → open pocket → take analgesic → take screwdriver → take toothbrush → take thing → south → take mail → south`

**Bulldozer / Ford:**
`lie down in front of bulldozer → wait (×3) → say to Ford "what about my home" → wait → take towel → follow Ford → west → drink beer (×3)`

**Vogon ship — babel fish:**
`smell → examine shadow → [in hold] put towel on drain → push dispenser button → [get fish into ear before robot grabs it]`
⚠️ Note: It's unclear from the log whether the babel fish was successfully obtained. The sequence was attempted but the robot kept grabbing it. **Verify babel fish is in ear at session start.**

**Transporter / arrival on Heart of Gold:** Solved. Score locked at 33 on arrival.

---

## 🚪 ACTIVE PUZZLE: THE INTELLIGENCE DOOR

**Location:** Corridor, Aft End → port
**Door text:** "Show me some tiny example of your intelligence, and maybe, just maybe, I might reconsider."
**Also requires:** Proof of time travel ability (per Guide entry).

**Intelligence definition (from Guide):** "The ability to reconcile totally contradictory situations without going completely bonkers — e.g., having a stomach ache and not having a stomach ache at the same time, holding a hole without the doughnut."

### ❌ EXHAUSTED — Do not try again

*Specific dismissals (door is aware of these, still refuses):*
- no tea
- The Hitchhiker's Guide
- pair of tweezers *(when Marvin is absent — see Marvin note below)*
- sales brochure
- spare Improbability Drive

*Yawns (door is unimpressed, not cosmically aware):*
- Advanced Tea Substitute / hot cup of ATS
- thing from aunt
- Sub-Etha signaling device
- toothbrush
- molecular hyperwave pincer

*Conversation attempts (parser failures or silence):*
- `ask door about intelligence` → not interested
- `ask door about time travel` → not interested
- `say I am lying` → treated as talking to self
- `say to door I am not intelligent` → parser rejected "not"
- `tell door that I am stupid` → parser rejected "that"
- `say to door I am a fool` → parser rejected "fool"

*Marvin interactions tried:*
- `ask Marvin about improbability drive` → silence, wanders off
- `ask Marvin to open door` → **"I think you ought to know I'm feeling very depressed."** *(only non-silence response Marvin has given)*
- `give [cup of ATS] to Marvin` → politely refuses
- `examine Marvin` → nothing special
- `follow Marvin` [while he's standing there] → "But Marvin is right here!" then he enters door
- `talk to Marvin` → looks at you expectantly, but no vocabulary matched

### 🔍 UNTRIED LEADS — Try these first

**Priority 1 — The Marvin angle:**
- `ask Marvin to open door` got his only real response ("I'm feeling very depressed"). This is Adams signalling something. Try following up: `ask Marvin about depression` / `ask Marvin about door` / `give [something] to Marvin` while he's still in the room.
- The timing issue: I tried `follow Marvin` while he was standing there, but he entered the door before I could act. Try issuing the follow command earlier — as soon as he enters the corridor, not after examining him.
- **Marvin's patrol route:** He visits Corridor Aft End, Engine Room, Bridge, and the room behind the door. He's on a multi-room circuit. The pattern suggests deliberate game design around him.

**Priority 2 — The Marvin + door interaction:**
- Tweezers got a SPECIFIC DISMISSAL when Marvin was present in the corridor, but only a YAWN when he was absent. The door's responses vary based on Marvin's presence. This means: what we show the door might matter more WHEN Marvin is watching.
- Try showing items to the door specifically when Marvin is standing in the corridor with you, not just any time.

**Priority 3 — The access space:**
- Hatchway → starboard. Entrance too narrow for multiple items — "maybe ONE thing."
- Never entered. Best candidate item to bring: tweezers (cosmically known to the door).
- What's in there? Completely unknown. Could be the answer to the time travel requirement.

**Priority 4 — Vocabulary search for paradox:**
- Parser rejects: not, that, fool, hello, lying
- Try: `show door true` / `show door false` / `say true to door` / `show door both` / `show door neither` / `say impossible`
- Target: find a word that lets me STATE a contradiction to the door rather than show an object.

**Priority 5 — The hatch below:**
- Hatchway has a closed hatch in the floor. Never tried opening or going through it.
- `open hatch` → `down` → explore what's beneath.

**Priority 6 — Screwdriver on the dipswitch circuit board:**
- See Other Unresolved section. If the Nutrimat produces real tea, that might interact with the door's "no tea" dismissal in a new way.

---

## 🔎 OTHER UNRESOLVED ELEMENTS

**Circuit board in the Galley (Corridor Fore End → port):**
- Location: Galley, inside Nutrimat/Computer Interface carton.
- Has 8 dipswitches: Cholesterol Register, MSG Specifier, Thiamin Stack, Piquant-O-Mat, Flavour Dump, Vitamin Interrupts, Nose Sequencer, Bouquet Arbitration Bus.
- Has a message in microscopic letters — too small to read. Tried: `read message with pincer` → "how does one look through a molecular hyperwave pincer?" 
- **Untried:** `use screwdriver on dipswitches` / `flip dipswitch 1` / `adjust circuit board` / `read message with tweezers` (they're small and precise)
- Theory: This is the Nutrimat configuration board. Changing the settings may change what the machine produces. The Corridor Fore End already had a hot cup of ATS spontaneously — possibly produced by the Nutrimat. **If the Nutrimat can be reconfigured to produce real tea, that changes the "no tea" dynamic with the door.**

**The Junk Mail:**
- Picked up at the house. Examined (demolition notice from two years ago). Carried through everything.
- Is there more to it? Try `read junk mail` more carefully, or check if individual letters matter.

**The Strange Gun (on Bridge):**
- Visible in inventory at move 403. Never examined closely, never used.
- Try: `examine gun` / `fire gun` / `shoot door with gun` (a long shot but Adams-appropriate) / `ask Eddie about gun`

**The Large Receptacle on the Bridge Console:**
- Tried putting in it: pincer, aunt's thing, gun, cup — all refused.
- The Spare Improbability Drive needs to go in here. It's currently in the Engine Room (dropped at move 679). **Pick up the drive and insert it into the receptacle.** Eddie says "I don't see any drive" — he needs to see it there.
- This may be required to advance the main plot regardless of the door.

**The Flathead Screwdriver:**
- Carried since the bedroom. Uses: adjusting dipswitches on circuit board (see above), possibly opening something, possibly the glass case in the Vogon hold.
- Has it been used for anything yet? If not, it's overdue.

**Score drop (moves 312–381):**
- 30 points lost somewhere in this range. The log section covering this wasn't read during synthesis.
- Check: what does the game consider a scoreable negative action? Losing 30 points is significant.

**Babel fish status:**
- The towel-on-drain maneuver was executed. Robot still grabbed the fish in some attempts. Unclear if babel fish successfully ended up in ear.
- If not in ear, Vogon poetry reading will be gibberish and the transporter sequence may be incomplete.

---

## 📋 NEXT SESSION PRIORITY ORDER

1. Verify babel fish is in ear (try to understand any Vogon speech encountered)
2. Pick up Spare Improbability Drive from Engine Room; insert into Bridge receptacle
3. Follow Marvin — from the moment he appears in Corridor Aft End, issue `follow Marvin` immediately (timing has been the issue)
4. When Marvin is in corridor: `ask Marvin about depression` → `ask Marvin about door` → try giving him things
5. Enter access space to starboard in Hatchway (bring one item — try tweezers first)
6. Examine and try screwdriver on Galley circuit board dipswitches
7. Try hatch below in Hatchway
8. Examine strange gun on Bridge
9. Vocabulary probe at door: `show door false` / `say impossible` / `show door both`

---

## 📝 SYNTHESIS NOTES

*Things found in the log that didn't appear in any after-action:*
- Marvin's "I'm feeling very depressed" response to `ask Marvin to open door` — this is his ONLY non-silence. Never followed up.
- Circuit board with dipswitches in the Galley — completely undocumented in after-actions.
- Score drop from 33 → 3 between moves 312-381 — cause unknown, gap unread.
- Tweezers got yawn (Marvin absent) vs. specific dismissal (Marvin present) — the door is not deterministic by item alone.
- The hot cup of ATS in Corridor Fore End appeared spontaneously — probably Nutrimat output.
- `give cup to Marvin` → "politely refuses" — another non-silence response. Also undocumented.
