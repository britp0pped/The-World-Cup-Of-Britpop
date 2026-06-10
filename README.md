# The World Cup of Britpop

Hello you. Make a cup of tea, put a record on.

Because ranking Britpop bands was apparently too calm, too sensible, and nowhere near likely enough to ruin friendships, we now have **The World Cup of Britpop**.

It’s a custom-built browser application designed to answer an impossible question with exactly the level of seriousness it deserves: **which Britpop band would win the World Cup?**

The format takes 48 qualifying bands, ranks them by public vote, seeds them into pots, and then lets the draw do its work. The public vote provides the order. The software provides the chaos. Everyone else provides the arguing, which is where the whole thing becomes properly useful.

## The draw

The 48 bands are divided into four seeded pots.

- **Pot 1** contains ranks 1 to 12.
- **Pot 2** contains ranks 13 to 24.
- **Pot 3** contains ranks 25 to 36.
- **Pot 4** contains ranks 37 to 48.

There are twelve groups, running from **Group A** to **Group L**. Each group receives one band from each pot.

The placement is fixed. The draw starts at Group A and moves through the groups in order. The application doesn’t sit there deciding that Group F needs a bit of emotional damage or that Group J looks undercooked. It simply selects one band at random from the relevant pot, places that band into the next group, removes it from the pot, and carries on.

A tournament draw, then. With guitars. And possibly a very tense discussion about Cornershop.

## The fairness bit

The draw uses JavaScript’s built-in random number generator, `Math.random`.

Every remaining band in a pot has an equal chance of being selected. Once a band has been drawn, it’s removed from that pot and can’t appear again.

The application also checks that the structure is right before the draw can run. There must be exactly four pots. Each pot must contain exactly twelve bands. No duplicate bands are allowed.

This matters because Britpop arguments are already quite capable of collapsing under their own fringe without the software joining in.

## The randomness bit

`Math.random` is a pseudo-random number generator. It isn’t true randomness, and nobody should pretend it’s been lowered from a Swiss mountain by a committee in blazers.

For a browser-based tournament draw, it’s entirely appropriate. It’s the same kind of approach used by countless websites, games, and web applications.

The important point is simpler: the software treats every remaining band in the same way. It doesn’t know whether it has selected Pulp, Oasis, Blur, Cornershop, or anyone else. It has no favourites. It has no taste. It has no old NME covers hidden under the bed.

## The build

The whole thing is a single-page web application built with HTML, CSS, and JavaScript.

There’s no server. No database. No API. No spreadsheet connection. No external randomisation service. Once the page is loaded, the draw runs entirely inside the browser window.

To run it, open `index.html` in a modern browser, or deploy the file using GitHub Pages.

No installation is required, which is more than can be said for the average Britpop opinion.

## The decoration

The project uses a small number of external resources for presentation only.

Kosugi is loaded from Google Fonts and used for typography and visual styling. It has no influence on the draw process or the results.

The opening animated title graphic is also hosted externally and appears on the holding screen. Again, it’s purely visual. It doesn’t affect the draw logic, unless you believe title graphics can intimidate JavaScript, in which case this may be a deeper issue.

## The AI disclosure

ChatGPT was used during development as a coding and design assistant.

It helped with HTML, CSS, JavaScript, debugging, user interface refinement, accessibility improvements, copywriting, and documentation.

ChatGPT doesn’t participate in the draw itself and has no influence over the results. Once the code was completed, the application became a standalone browser-based tool.

The machine helped build the room. It doesn’t pick the bands in it.

## Why this exists

Because ranking Britpop bands was only the start.

Now they have to survive the group stage as well.

This, as always, is then.
