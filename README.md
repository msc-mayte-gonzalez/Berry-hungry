# Berry Hungry

**A browser survival game that teaches real plant-foraging safety — can you tell the edible plant from its poisonous look-alike before your hunger runs out?**

▶️ **Play it here:** [ADD YOUR NETLIFY LINK HERE]

---

## What it is

You're lost in the forest with no food and a rescue helicopter on the way — if you can survive long enough. Along the path you'll run into pairs of real, look-alike plants: one edible, one poisonous. Pick correctly and your hunger refills; pick wrong and it costs you. Run out of hearts before the helicopter arrives, and the run ends.

It's built to make a real skill — telling a safe plant from a dangerous one — feel like something you *practice*, not something you're just told.

## How to play

- Walk forward automatically while your hunger meter ticks down.
- When you reach a plant pair, you're shown a real reference photo of each — pick the one that's safe to eat.
- A correct pick refills your hunger. A wrong pick drains it sharply.
- Hunger hitting zero costs you a heart. Lose all your hearts, and it's game over.
- Survive long enough, and a helicopter arrives to rescue you.
- Currently a desktop experience — see **Project status** below.

## Screenshots

*Add 2–3 screenshots here (title screen, a plant encounter, and the win or game-over screen work well).*

## Plant pairs featured

| Edible | Poisonous look-alike |
|---|---|
| Downy hawthorn | Winterberry |
| Wild grape | Canada moonseed |
| Purslane | Spurge |

Every identification and toxicity claim was cross-checked against at least two independent botanical/toxicology references before being used in the game, and every photo's license was verified individually before use (see **Credits** for sources).

## Built with

| Tool / Resource | Used for |
|---|---|
| Claude (Cowork / Claude Code) | AI build partner — wrote, tested, and explained every round of code changes |
| GitHub | Version control; two-contributor commit history across branches and pull requests |
| Sourcetree | Local Git client used to review and apply every change |
| Netlify | Hosting, with auto-deploy on every push |
| PostHog | Product analytics — funnel tracking, drop-off, custom events |
| Playwright | Automated browser testing; one regression-test file per build round |
| Photoshop | UI asset creation (hearts, meters, card frames) |
| Wikimedia Commons, iNaturalist, USDA PLANTS, Bugwood | Sourcing licensed, credit-cleared plant photography |
| Illinois/Minnesota Wildflowers, Missouri Botanical Garden, Go Botany | Fact-checking plant identification and toxicity claims |

Three.js and `<model-viewer>` were evaluated early on for a live 3D forest scene; the team prototyped the pipeline, confirmed it worked, and chose a simpler 2D build anyway to ship something that loads instantly and runs identically on every device.

## Running it locally

No build step, no dependencies — it's a single HTML/CSS/JS file.

```
git clone <this repo>
cd <this repo>
open index.html   # or just double-click it
```

## Project status

This is a living prototype — you'll see a "prototype · placeholders throughout" tag in the game itself. Known scope:

- **Desktop only, for now.** Mobile support was attempted (a forced-landscape mode with on-screen touch controls) and then intentionally pulled back after real-device testing showed the layout wasn't good enough to ship. Phones and tablets currently see an honest "built for desktop, for now" message instead of a half-working experience.
- Art and audio are placeholder-ready: dropping correctly-named files into `images/`, `sounds/`, and `music/` lights them up automatically — see the `README.txt` in each folder.

## What the analytics showed

*Once there's real traffic, put 2–3 numbers here — for example: unique players, average time played, win rate, or the most common drop-off point. PostHog is already tracking all of these.*

## Credits

- Idea, info collection, user research, design, and prompting by M. Gonzalez (Sr. UX Researcher).
- Art by anonymous collaborator (a great 3D Environment Artist, I wish I could tell you who!).
- Built with Claude.
- Supervision by H. Botones (our hedgehog).
- Music: [Nathan-180](https://pixabay.com/users/nathan-180-56136572/) via [Pixabay](https://pixabay.com/music/).
- Sound effect: [freesound_community](https://pixabay.com/users/freesound_community-46691455/) via [Pixabay](https://pixabay.com/).
- Sound effect: [Ghostie Graves](https://pixabay.com/users/shut_up_ghost-32917765/) via [Pixabay](https://pixabay.com/).
- Downy hawthorn photography: [Ashley Adamant](https://practicalselfreliance.com/hawthorn/).

## Disclaimer

This game is for educational purposes only. It does **not** replace hands-on foraging training. Never eat a plant unless you can identify it with certainty. Unlike in this game, you don't have extra hearts or a chance to start over.
