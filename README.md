*Este readme está escrito en INGLÉS. Si lo prefieres, puedes leerlo en [español](README.es.md).*

# Figurante

Detective video game set in a carnival crowd. Made in Unity, C#, during the Global Game Jam 2026 (48 hours) at Teatro Argentino, La Plata.

You can play the game on [itch.io](https://manuellegago.itch.io/figurante).

## Technologies

Developed using:
- C# Language
- Unity 6.3 LTS (URP 2D)

*You can see the code [here](Assets/_Scripts/).*

## Controls

- Move: W A S D
- Talk / Accuse: hold Space for 1 second
- Pause: Esc or P

## Idea and development

A new carnival season begins and someone is planning a murder. The only clue is an anonymous note found at the entrance.

The goal was a short deduction game where you read a crowd instead of a crime scene: infiltrate the carnival, listen to witnesses and rebuild the mask of the person who left the note before the night ends.

## Implementation

Every guest wears a mask built from three random features: hat, ornament and eyes. The crowd has 60 guests and only one of them has the killer's combination.

After the tutorial, some guests become witnesses and raise their hands over time. Each one remembers one feature, but not all of them tell the truth: for every feature there are two false and two true testimonies. A feature is confirmed on the identikit only when two witnesses agree.

The clock runs from 23:58 to midnight while a carriage advances along the street. Accusing the right guest wins the game; a wrong accusation, or reaching midnight, ends it.

## Links and credits

- Development: Tomás Marmoni ([tdm1094](https://github.com/tdm1094)), Germán DiFrancesco ([GermanDiFrancesco](https://github.com/GermanDiFrancesco)), Facundo Bravo
- Narrative: Facundo Bravo, Fera Zuccarelli
- Art and design: Fera Zuccarelli (mask assets by [Freepik](https://www.freepik.com))
- Sound and music: Manu Elle ([itch.io](https://manuellegago.itch.io))
- Font: Adelphe
