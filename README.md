# MHS3 — Monster Hunter Stories 3 Factual Reference Skill

A Claude skill that prevents LLM hallucination of Monster Hunter Stories 3: Twisted Reflection facts. Routes queries through [SKILL.md](SKILL.md) to one of 14 domain cheat sheets, with 39 grep-addressable PSV lookup files (5,200+ rows) for deep detail. Run `python3 .xlsx-source/extract.py` to regenerate the PSVs after a patch.

## Data Sources (all credit to these projects)

All factual data in this skill was extracted from or cross-referenced with:

- **Full game datamine** — [docs.google.com/spreadsheets/d/1JvLmNY7l2jOKCk7QbUYmeK87xvzQzXVUJIgFX9bYaqk](https://docs.google.com/spreadsheets/d/1JvLmNY7l2jOKCk7QbUYmeK87xvzQzXVUJIgFX9bYaqk/edit?gid=603086227#gid=603086227) (147 sheets of game tables)
- **MHS3 monstie stats** — [docs.google.com/spreadsheets/d/1p5N1NJAN1SGvWG1hQ7kzKkkwSnjm70eHBPYYovG0U64](https://docs.google.com/spreadsheets/d/1p5N1NJAN1SGvWG1hQ7kzKkkwSnjm70eHBPYYovG0U64/edit?gid=0#gid=0) (88 monsties with full stats + bingo bonuses)
- **MonsterBuddy** — [monsterbuddy.app/3](https://monsterbuddy.app/3) (monsties, monsters, eggs, habitats, egg-powers, genes, riding-actions)
- **Capcom official manual** — [manual.capcom.com/mhst3/en/switch2/](https://manual.capcom.com/mhst3/en/switch2/) (scraped to `.xlsx-source/capcom-manual/`; 213 items across 9 categories)
- **Les Carnets de la Wycadémie** (Masuku) — [Building the Perfect Monstie](https://lescarnetsdelawycademie.fr/building-the-perfect-monstie/) and [Wyvernfell](https://lescarnetsdelawycademie.fr/wyvernfell/) essays for advanced mechanics and formulas
- **Reddit stamina guide by /u/TheMobDylan** — [r/MonsterHunterStories/1sobnlk](https://www.reddit.com/r/MonsterHunterStories/comments/1sobnlk/guideresource_a_basic_stamina_guide_for_mhs3/) for stamina archetypes and rotation breakpoints
- **Game8 MHS3** — [game8.co/games/Monster-Hunter-Stories-3](https://game8.co/games/Monster-Hunter-Stories-3/archives/586383) for the tier list (updated April 7, 2026)
- **mhstories3.wiki** — [mhstories3.wiki](https://mhstories3.wiki) for general wiki reference

Huge thanks to the datamine authors, MonsterBuddy team, Masuku, TheMobDylan, Game8 writers, and the r/MonsterHunterStories community. This skill is merely a structured reformatting of their work so LLMs stop hallucinating. All factual credit belongs to them.
