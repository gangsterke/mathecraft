# MatheCraft – plan and decisions

## Rules
- Content is organised by the four areas of the primary school maths curriculum. All explanations, pictures, exercises, characters and games are our own and written from scratch.
- Each lesson uses our own structure (five steps), our own story with Leo, our own pictures (base-ten blocks drawn in our colours, the place-value ladder) and generated exercises.
- Mascot: Leo the lion, a plush lion (our own picture). Leo is a boy (he / er).
- No copies of known game characters: all games are our own designs.
- Place-value colours: ones / thousands / million green, tens / ten thousands blue, hundreds / hundred thousands red.
- Every new text goes into the translation table in all three languages (de, en, es).
  - Place-value abbreviations: de M HT ZT T H Z E · en M HTh TTh Th H T O · es Mi CM DM UM C D U
  - Number format: de / es 1 000 000, en 1,000,000

## Domains
- mathecraft.de (German) and mathcraft.eu (international)

## App
- Language switch DE / EN / ES in the top bar (remembered per device).
- Kid area: star balance, today's stars and minutes, game cards with pictures, lesson list (including the number word trainer), trophies (10 / 25 / 50 / 100 / 250 / 500 stars).
- Required tasks: entering a lesson or the trainer requires N finished tasks (default 10) before going back. Parent setting, 0 = off.
- Parent area (PIN): stars, learning and play time, 14-day chart, accuracy per task type, lesson and trainer summary (most common mistakes), activity log, game test buttons (no stars, not logged), settings (name, games on/off, price, minutes, required tasks, PIN), bonus stars.
- Games (default 10 stars = 3 minutes, each with its own record): jumping game (runner over blocks), flying game (plane shoots falling bombs), space flight (rocket dodges rocks, collects stars), hedge maze (cookies, rain clouds, stars give a shield; swipe or arrow buttons). Touch steering is relative to where the finger lands; the iOS selection menu is disabled in games.
- Read aloud: speech rate de 0.75, en / es 0.6; trainer words a little slower.
- Stars: practice and trainer rounds always earn; the quick test earns stars on at most 3 tests per day; puzzles earn on the first try (Pro puzzle = 2).
- Look: one bright, light theme (no dark mode).

## Number word trainer
- Target language DE / EN / ES (independent of the site language), levels up to 100 / 1,000 / 100,000 / 1,000,000, automatic level-up at 7 of 8.
- Mistake rules with tips (ß, sechzehn / sechzig, siebzehn / siebzig, ein / eins, word order, forty, eighteen, ninety, dieciséis, veinti…, quinientos, cien / ciento, un mil …). Spanish answers with only missing accents count as right, with a note.
- Also available as the task type "write in words" in practice rounds.

## Lesson template
1. Understand: illustrated step-by-step story with read-aloud
2. Remember: place-value ladder (×10 steps) and one number shown four ways
3. Test: 4 generated multiple-choice questions, new every time
4. Practise: endless generated rounds of 8 tasks, hints, stars (progress boxes: green first try, light green second try, red wrong)
5. Puzzles: 3 generated puzzles and 1 Pro puzzle, with answer boxes

## Going public
- Web app (PWA) on mathecraft.de / mathcraft.eu, parent accounts, database in an EU region. Free start; a small yearly price or donations later.
- Steps:
  1. Trademark check of the name (DPMA, EUIPO, TMview)
  2. Code on GitHub, static hosting plus an EU backend
  3. Impressum, privacy policy, data processing agreements
  4. Free beta with a few families
  5. Payments later via a merchant-of-record provider

## Curriculum map (grade 4), all lessons built ✅
- **Numbers and calculating:** Building a million · Big numbers made easy · The number line · Number patterns and neighbours · Rounding · Written multiplication · Written division
- **Shapes and space:** Right angles, parallel and perpendicular · Quadrilaterals · Patterns and tilings · Area and perimeter · Cubes and volume
- **Measuring:** Millimetres to kilometres · Grams, kilograms, tonnes · Litres and millilitres (incl. ⅛ l) · Time and durations · Converting measures
- **Data and chance:** Charts · Chance and probability
- Always available: number word trainer (DE / EN / ES)

## Next
Split the website into index.html + lessons/*.js · grade 3 and grade 5 content · more games (including children's own game ideas)

## How lessons are built
Each lesson is one `defLesson(id,{…})` block: story steps, remember box, quick-test generators, practice generators (each returns its answer key `a` for automatic testing), puzzles and Pro puzzles. All texts are `{de,en,es}` objects.
