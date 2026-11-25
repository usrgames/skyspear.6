# Skyspear

The releases of Skyspear, a block-building game of a prehistoric lost world for the terminal, from [usr.games](https://usr.games). Its page is [usr.games/skyspear](https://usr.games/skyspear), where it also plays in the browser.

This repository holds what a player downloads and the game's rules, and none of its source.

![A cave person at a camp by night, seen from behind: the comet among the stars, the smoke of the camp's fire going up, and the red glow of a fire mountain far off, drawn in terminal cells](docs/shot.png)

A block-building game of a prehistoric lost world, in the terminal, built on [glonk](https://glonk.dev). You are a cave person among dinosaurs, fire mountains and falling stars, and you begin with nothing. Each night a comet grows among the stars, and on the twelfth it arrives. Make fire, hunt or hide, paint what you have met, and win the trust of a camp until its people come to live at your fire.

- **Lands older than grass,** in a world with no end made from a seed: a prairie of ferns, a jungle of tree ferns, a highland of redwoods, red badlands with the skeletons of great beasts, a coal swamp with tar pits, a cold steppe, and the sea. A journey off stands a fire mountain, with hot springs at its foot, and every few days it erupts.
- **Twenty-two kinds of beast:** herds of buglers, quickclaws that hunt by night and keep out of light, giants whose steps shake the ground, and the dread, which hunts everything. Steal an egg, hatch it by a fire, and ride what grows from it; a galewing carries you in a glide.
- **Stone tools and fire:** flint is knapped into tools, a spear is thrown and a sling throws pebbles. Fire is found in a tree that lightning struck, carried as a torch, and made with a drill in a hearth, which cooks.
- **A sky that falls:** stars come down and leave sky iron. The comet is the Skyspear, and when it arrives it brings the Great Fall, and after it the Long Winter: four days of ash, frost and cold.
- **Paintings and people:** paint what you have met on rock, and read it back as a record. People live in camps and trade by showing, and those who trust you come to your fire to keep it, gather, knap and guard it.

Play in survival, where you dig what you need, eat and stay alive, or in creative, with every block and nothing to fear. You see through your own eyes or from behind your shoulder. The art and the sounds are original, made in code.

## Install

With [tty1](https://usr.games/tty1), the usr.games launcher:

```
tty1 install skyspear
```

Or by hand, from the [latest release](https://github.com/usrgames/skyspear.6/releases/latest): take the archive for your system, `skyspear_OS_ARCH.tar.gz` (`darwin` or `linux`, `arm64` or `amd64`), with `manifest.json` and `manifest.json.sig`. Check them as [KEYS.md](https://github.com/usrgames/usr.games/blob/main/KEYS.md#check-a-release-by-hand) says, then unpack the archive and run `./skyspear`. Its manual page, `skyspear.6`, is in the archive too.

- **Use a terminal that reports key releases:** Ghostty, kitty, WezTerm, foot, iTerm2 or Alacritty. There you can walk and turn at once. In other terminals (Apple's Terminal, for one) only one key stays held at a time, which is playable but clumsy, and the game says so on screen. This is how glonk reads keys; see its README.
- **A bigger window is a sharper picture.** Every cell is two pixels, one above the other, so 200 by 60 cells is a picture of 200 by 120 pixels.
- **True color looks best.** Inside tmux or over ssh, `export COLORTERM=truecolor` if your terminal can show it.

## Report a fault

[Open an issue](https://github.com/usrgames/skyspear.6/issues/new) here. Say what you did, what happened, which terminal you use, and what `skyspear -version` prints.

## Keys and mouse

| Keys | Action |
|---|---|
| W A S D | walk, strafe; in a galewing's glide, W dives and A and D turn |
| Arrows | look |
| Space | jump; swim up; rise when flying; on a beast you ride, jump or charge |
| X | sink when flying |
| F | flying on and off, in creative |
| C | crouch, and stand again: slow, low and quiet; on a beast you ride, get down; in a glide, let go |
| V | the view: through your eyes, or from behind your shoulder |
| L | the next of sixteen looks for your body |
| Q / E | break / place the block aimed at (hold to go on); hit / shear a creature aimed at; either takes an egg aimed at, and E with an egg in hand puts it down; E with food in hand eats it, or feeds a young beast of yours, or a snowtusk calf, aimed at; E on a grown bugler, shieldbrow or snowtusk of yours gets on it; E with a paint in hand on a face of rock opens the pictures you can paint there, and on a painting with anything else in hand shows what you know of it; E on a clay pot or a hearth opens it, on a fur bed lies down, and on a fire lights the unlit torches in your hand; hold E with a fire drill on a hearth to light it |
| R | throw the spear in your hand, or with a sling in your hand a pebble (hold to go on) |
| 1 to 9, Tab | pick a slot of the hotbar; the next one |
| I | your things: move them between the hotbar and the pack, and make things from them (in creative: every block) |
| T | move the clock on six hours |
| F3 | frame numbers: where the time of a frame goes and how much is sent, the seed, the day and the hour, the days until the comet arrives and until a star next falls near you, and within 300 blocks of a fire mountain the days until it next erupts |
| Esc | pause menu, with these keys on it; on a menu, back |

| Mouse | Action |
|---|---|
| Move | aim at the block under the pointer |
| Hold left and drag | turn the view |
| Left click / right click | break / place (hold still to go on); hit / shear a creature |
| Wheel | pick a slot |
| Click a hotbar slot | pick that slot |
| Click in the bag (I) | take what is in a slot, or put down what you hold; make a line of the list |
| Move and click on a menu | pick a line and choose it |

- **Whichever you used last aims.** Move or click the mouse and the pointer aims. Press an arrow key and the middle of the view aims again, with its crosshair.
- **Drag to look.** A terminal reports the pointer in cells and cannot lock it, so the view cannot follow the mouse as it does in a window. Holding the left button and dragging turns it, a cell at a time; a press let go where it is stays a click. The arrows turn it too.
- While the game runs, the terminal cannot select text with the mouse. `-mouse=false` gives the pointer back to it.
- Letters work in either case, and Ctrl-C quits (and saves).

## Your first night

Make a new world in survival. The first night of a world is quiet, so use the first day and night to get ready for the second.

1. **Wood and fiber.** Break a tree trunk with Q, by hand, for logs. Press I to make four sticks from a log. Break ferns or tussocks of dry grass for fiber: three make a cord.
2. **Stone and flint.** Break stone for cobble, and a flint seam or gravel for flint. Four cobble make a knapping stone. Put it down, stand by it, and knap a hand axe, a flint knife or a flint pick.
3. **A fire.** Eight cobble make a hearth. Put logs in it, make a fire drill (a stick, a log and a cord), and hold E on the hearth with the drill for six seconds. A log burns for 80 seconds, and a night is five minutes, so give it four.
4. **Food.** Q on a bush gives berries. A full stomach lasts a day. A hearth cooks meat: 12 points of food against 5 raw.
5. **The second night.** Quickclaws come, in packs of two or three. You cannot outrun one, but it stops about four blocks from a torch or a hearth that burns: stay in the light. Make a spear from three sticks. A torch is a stick and resin, which one pine or redwood log in five leaves. Light it at the fire and set it down, and it burns for ever.
6. **Later.** A fur bed (3 hides and 6 moss) is where you wake, and at night it sleeps you to the morning. On the steppe the daggercat hunts by day. From the third morning the dread may come, and only three fires close together hold it. The comet arrives on the twelfth night.

## Survival and creative

**New world** asks how the world is played, and the world keeps that.

- **Survival.** You start with nothing. A block takes time to dig, from a fifth of a second for leaves to five seconds for stone by hand, and cracks show as you dig. Let go, or look away, and it starts again. A broken block drops as a small block of itself (stone as cobble, mossy earth as dirt, a bush as berries, a fern or a tussock of dry grass as fiber, a flint seam as flint, ochre as ochre and chalk as chalk, and one block of gravel in eight as a flint; leaves crumble away), which you pick up by walking near. You carry 9 slots on the hotbar and 27 in the pack, 64 of a kind to a slot, and placing a block uses one up.
- **Your body.** Health, food and air show over the hotbar. A fall of more than three blocks hurts, a point for each block more, but not into water. Under water your air lasts 15 seconds, then you drown, slowly. Food goes down a point every 30 seconds; while it is 18 or more of 20 you heal, and at none hunger hurts, though it cannot kill. Berries from bushes, fruit from now and then a leaf, and meat are food. Standing in a fire hurts, 2 points a second. Warmth is a fourth bar, over your health, that shows only when you have lost some: the cold takes it, and a fire gives it back.
- **Making things.** The I screen lists what you can make, beside your slots: Right from the last column goes into the list, and Enter or a click makes one. A line is dim while you lack something for it, and what a line needs shows under the slots. By hand you make four sticks from a log, a cord from three fibers, a knapping stone from four cobble, a digging stick (2 sticks), a club (a log), a spear (3 sticks), a fur bed (3 hides and 6 moss), a hearth (8 cobble), a fire drill (a stick, a log and a cord), two unlit torches (a stick and resin), a soft pot (4 clay), a sling (2 cords and a hide), four pebbles (a block of gravel) and two pit covers (2 sticks and 2 fibers). Stand within four blocks of a knapping stone to knap flint: a hand axe (2 flint), a flint knife (a flint, a stick and a cord) and a flint pick (3 flint, 2 sticks and a cord). There too you grind paint: four red of a piece of ochre, four black of a coal, four white of a piece of chalk. Planks, the workbench, the kiln, the crate, torches of coal and the tools of copper and iron can no longer be made; a world that has them keeps them.
- **Fire is found.** Here and there stands a tree that lightning struck: a charred trunk that burns at its top, with a limb that fell from it burning at its foot. Its smoke stands nine blocks over it by day, and its fire shows at night. No hand breaks a fire, and no block takes its place: it goes when the log it burns on is broken. A charred log leaves coal.
- **Fire is made.** A hearth is a ring of stones. Put wood or coal in it, then hold E on it with a fire drill for six seconds, or press E on it with a lit torch. A fire drill lights twelve fires.
- **A hearth burns and cooks.** E on a hearth opens its three slots over yours: what to cook, its fuel, and what it has made. Lit, it burns its fuel a piece after another whether it cooks or not, and goes cold when the fuel is gone: a stick lasts 15 seconds, a log 80, coal 160 and peat 240. While it burns it gives light, smokes, and cooks a piece in six seconds: raw meat to cooked meat (12 points of food, against 5 raw), the seeds of a stump palm to roast seeds, a spear to a hardened spear (it hits for 4 and lasts 150 uses), a soft pot to a clay pot, clay to brick, and a log to coal, which is charcoal. A hearth goes on burning when you leave it, wherever it is.
- **Torches.** E on any fire, a lit hearth or a torch that stands lights the unlit torches in your hand. A lit torch in your hand lights the ground round you as you walk, and quickclaws keep out of that light as they do any. It burns for five minutes in the hand, in survival, and then it is a stick again. Set down, a torch burns for ever.
- **Resin and seeds.** One pine or redwood log in five leaves a piece of resin with the log. The crown of a stump palm leaves two seeds: raw they are poison, 4 points of health for 2 of food, and roast they are 6 points of food.
- **A clay pot keeps things.** E on a clay pot opens its 18 slots over yours. What is in a pot or a hearth falls out when you break it.
- **A fur bed** lies flat on the ground. E on one makes it where you wake, after a faint too. At night it also sleeps you through to the morning, unless a hunter is within eight blocks. A broken bed is forgotten, and you wake where you first began.
- **Ochre and chalk** are what paint is made of. Ochre lies in beds in the red rock of the badlands, red and yellow in streaks, and shows as bands on the sides of the mesas. Chalk lies in white beds in the stone near the top of every land, with nodules of flint in it: cliffs and caves show it. Both break by hand. Paint is ground from them at a knapping stone, and black paint from coal.
- **Painting.** E with a paint in hand on a face of rock opens the pictures you know, in a row: to start, a hand and a spiral, and then the comet and every beast you have met. Left and Right choose, Enter paints and uses one paint, Esc leaves. Rock is stone, cobble, red rock, sandstone, basalt, chalk and deepstone; earth, wood and leaves take no paint. The picture fills the face, in the paint's color, and takes the grain and the light of the stone under it. The hand is a stencil, as in real caves: paint blown round a hand, which is left bare. Paint over a painting to change it. Break the block and its paintings are gone; a block put against one hides it until that block goes.
- **What you have met you can paint.** A beast is met when you see it within 32 blocks with nothing in the way, or when it hits you or you hit it: "you have seen a daggercat: you can paint it now". The comet is met the first night you see it from under the open sky. A beast is painted side on as a solid shape, made from its own body: a dread long and low, a cloudgrazer all neck. A long row of pictures scrolls as you choose.
- **A painting is a record you read.** E on one, with anything but paint in hand, shows its card: the picture large, its name, and what you know of it. A beast's card says in two to four lines what it eats or fears, what it does to you, and how it is won or killed. The comet's counts the nights until it falls, by the clock. A hand's says "you were here". Esc or E closes it. E on a painting is taken for reading, as E on a hearth is, so build against a painted face from another side.

![A cliff of stone with paintings on it: a shieldbrow in black, a daggercat, a bugler and a spiral in red, and a hand and the comet in white, with red paint in hand](docs/painting.png)

![The card of the painted daggercat, open over the cliff: the picture large, and under it its name and what you know of it](docs/card.png)

- **Camps.** Other people live in the green lands, the prairie, the highland and the jungle, in camps the seed puts there: a fire on a ring of stones, on ground made level round it, and two or three huts of hide stretched over poles. The first lies 120 to 200 blocks from the middle of the world, and you begin on open ground near that middle. A camp's smoke stands high, so you see it from far off. Three to five people live in a camp, no two alike. By day they walk about it, and at night they sit round its fire. Come within 10 blocks and each shows over their head, in a picture, what they want: amber, a tusk or crystal, meat, hide, flint or ochre. A camp's fire goes out only if the stone under it is broken, and then the camp has nobody. A hut breaks into hide. A world made before camps has none in the ground it had already made.
- **Trade.** Hold a thing and press E on a person. If their camp wants it, they show over their head what they would give for one, with how many, and E again while they show it trades. For anything else, or an empty hand, they show what they want. Each camp wants one precious thing, amber, a tusk or crystal, and two plain ones, and gives flint or resin and two dear things: cooked meat, a clay pot, a hard spear, obsidian or a fur cloak. The more a thing is worth, the more they give for it. Crouch and press E to give one as a gift: they give nothing back. After a trade or a gift they hold up a hand in thanks, and want the next thing their camp wants. A camp trusts you a little more for each trade, more for each gift, and most when you kill a hunter or a guard beast within 48 blocks of its fire, where its people see it.

![A camp on the prairie by day: huts of hide on poles, people by its fire, its smoke going up, and two cloudgrazers behind](docs/camp.png)

![At a camp by day, two people show over their heads what they want, one meat and one crystal, by the fire on its ring of stones](docs/want.png)

- **Your fire.** Your fire is a hearth within 8 blocks of the bed you last lay on, lit or not. When a camp trusts you enough, one of its people shows a fire over their head: they would come to live at yours. E with an empty hand says yes. With no fire yet they show what is missing: a bed, or a hearth by it. One who comes follows you, and runs to catch up when far behind. Leave them more than 104 blocks behind and they find their own way, and are at your fire by the next morning. At your fire they walk about it by day and sit round it at night, each in a place of their own. A camp asks first at a trust of 8, and again at 16, so two may come from a camp, and six live at your fire at most. One who came is not found at their camp again. E on one of them and they hold up a hand. At night two or more round a fire make music.
- **Work.** Show one who lives at your fire a thing, with E, to give them a job; show another to change it, and they put down what they carried. Wood, or anything that burns, and they keep your fire: every two seconds they put fuel from the pots by your hearth, within 4 blocks of it, into it when it runs low, put the raw meat from them in to cook, put what it has cooked back into the pots, and light it again if it has gone out. Berries, and they gather: by day they go out up to 24 blocks from the fire, pick up what lies on the ground and pick the bushes, and when they have four things, or there are no more, bring them to a pot by the fire, or put them down by it if no pot has room. They pick a bush as you do, so it is gone. A thing they cannot reach in 30 seconds they leave. Flint, and they knap: by day, at a knapping stone within 4 blocks of your hearth, they make a tool every ten seconds from what the pots by it hold, a hand axe, a flint knife or a flint pick, whichever the pots hold fewest of, until they hold two of each, and put it in a pot. A spear, and they take it and guard: day and night they stand 6 blocks out from the fire, at the edge of its light, facing out, run at any hunter or grown guard beast that comes within 12 blocks of it, and strike it with the spear once a second. Guards read your paintings: they go out after any beast of a kind painted within 16 blocks of your fire, up to 40 blocks from it. They let be what cannot be hurt, what is yours, and what swims or flies. They work while you are near enough for them to move, and a save keeps each one's job and what they carry, a guard's spear too.

![Your fire at night: a hearth that burns, two of your people sitting by it, and a guard with a spear at the edge of its light](docs/tribe.png)

- **Tools.** The right tool digs its blocks faster: a pick stone and ore, an axe wood, a shovel earth, sand and snow. A digging stick is a shovel of wood, twice as fast as a hand, and a hand axe and a flint pick are three times as fast, an obsidian pick four, and a pick or an axe of sky iron six. Stone, cobble and flint seams break by hand and leave what they hold; coal leaves nothing without a flint pick, and crystal nothing yet. A tool wears by a block broken or a beast hit, a bar on its slot shows what is left, and it is gone when it is worn out: a hand axe after 60, flint on a handle after 130, obsidian after 40, and sky iron after 400. Tools are one to a slot.
- **Weapons.** A hand hits for 1 point and a tool for 2. A club hits for 4 and knocks a beast nearly twice as far back. A spear hits for 3 and reaches a beast a block farther than anything else does. A flint knife hits for 4, and a kill made with it leaves one more piece of meat and always a hide.
- **Hides.** A bugler or a quickclaw leaves a hide when it dies.
- **Beasts.** A beast in front of a block is aimed at before it. Q or a click hits it, again every third of a second while held, and knocks it back. A blade hits hardest, from 3 points in wood to 6 in iron, any other tool 2 and a hand 1; a hit wears the tool in hand.
- **Mossbacks** graze alone on the moss. One cannot be hurt: it runs. E on a mossback shears its moss, which grows back in five minutes, with anything in hand but food.
- **Taming.** E on a mossback with berries or fruit in hand feeds it. After three meals it trusts you: it follows you, runs to catch up when it falls behind, and stands by you when you stand. A tame mossback is kept with the world however far you leave it, and takes no wild one's place.
- **Nippers** are the size of a hen and go in flocks of three to five on the prairie and in the jungle. Come within five blocks and the flock scatters. Stand near with food in your hand and one darts in from up to nine blocks, takes a piece and runs. A nipper has 3 points of health and leaves one piece of meat.
- **Buglers** go in herds of five to eight on the prairie and in the highland, three blocks tall, with their young, half as big, in the middle. A herd keeps together. Come within nine blocks of one, or within four crouched, and it gives its alarm and the whole herd runs from you, faster than you can. A running bugler that runs you down takes 3 points and throws you. A bugler has 16 points of health and keeps its hurts, and the herd runs each time you hit one.
- **The fire mountain.** 500 to 800 blocks from where a world begins stands a cone of dark rock 80 blocks across and about 40 over the land, with a crater at its top. Others lie one to every square of 1,600 blocks.
  - **You find it by its smoke.** From up to 1,200 blocks off a dark column stands in the sky in the way to it by day, and a red glow by night. It is drawn by the sky, so it shows far beyond the 64 blocks the land is drawn to, and it is fainter the farther off you are.
  - **Ashlands** lie round it, out to 70 blocks from its middle: grey ash, dark rock and a charred trunk here and there. Nothing grows there and no beast lives there.
  - **Lava** fills the crater to four blocks under the rim. It glows as fire does. You sink and swim in it as in water, it takes 6 points a second, three times what a fire takes, and the walls of the crater are too high to climb out by. What falls in it is burnt up. A torch can be lit at it. It cannot be broken or carried, and beasts keep out of it.
  - The crater smokes: great puffs that stand nine blocks over it.
  - **Obsidian** runs in black veins on the cone, more of them toward the top, and nowhere else in the world. A flint pick breaks it out.
  - **Firestone** lies in a ring at the rim of the crater, within three blocks of it: lumps the color of brass in the dark rock. It breaks by hand.
  - **Hot springs** lie on the ash 50 to 60 blocks from the middle of the mountain, three or four to a mountain: a pool of warm water one block deep, in rings of rust, gold and green stone. Stand in one and you heal twice as fast, if you have eaten enough to heal at all.
  - **Geysers** stand in the middle of some pools: the first of a mountain's springs always has one. Every 30 seconds a geyser spouts water and steam for three seconds, and the ground trembles for two seconds before. Stand on it when it goes and it throws you about twelve blocks up: come down in the pool and the fall does not hurt. Each goes at its own moment.
  - **It erupts,** every four to seven days, on days the seed gives it, and each mountain on its own. You know of it only within 300 blocks of the crater.
    - **A minute of warning.** The ground trembles, more and more, the mountain rumbles, and every beast within 100 blocks of the crater runs from it.
    - **Then a minute and a half of burning rocks.** One leaves the crater every three quarters of a second, arcs high with a trail of fire, and comes down on the ash, 14 to 64 blocks from the middle. One that hits you or a beast takes 10 points. A roof stops one: the lava tube is shelter.
    - **Where a rock comes down** it leaves a block of dark rock, or one time in four of obsidian, with a fire on it that burns out in a minute. In water or lava it leaves nothing.
    - **No rock comes down within 24 blocks of your bed.**
    - **Ash darkens the sky** from the first rock, and thins for half a day after the last: the light of day is down to a little over half under the most of it, which is still day to a quickclaw. From 200 to 300 blocks off you get less of the ash and of the tremor.
    - From far off the foot of the mountain's smoke is red by day, as it is by night.
  - **A lava tube** runs level into the side of the cone, two blocks wide and three high, lit by lava that still hangs in its roof. 23 blocks in is a chamber with a pool of lava in its floor, and obsidian and firestone in its walls. The dread is too big to follow you in.
- **Falling stars.** A few shooting stars a minute streak the night sky. About one night in three, at a moment in the dark that the seed picks, one comes down near you.
  - **A fireball crosses the sky** for four seconds, with its tail behind it, and the night under it is as bright as dusk. The sky draws it, so you see it from farther off than the land is drawn.
  - **It strikes 40 to 90 blocks from you,** or a little farther if a hill is in its way, on dry land. You see the flash at once. The boom comes a second later for each 40 blocks, so you can count how far, and the ground shakes with it.
  - **Never near what must be kept:** not within 24 blocks of your bed, nor within eight of a pot or a hearth, nor on a fire mountain. One that would come down there burns up: a flash and a boom, and no crater.
  - **It leaves a crater,** a bowl seven blocks across and three deep. What stood over it is gone. Its floor is burnt to dark rock, and where the ground was sand the bowl and its rim are glass. A beast or a person in it when it strikes loses 12 points.
  - **Five fires burn round it for a day.** This is fire you can find: light a torch at one and carry it home.
  - **Under the middle lies the core, of sky iron.** For two minutes it glows, burns you if you stand on it, 2 points a second, and nothing breaks it. Then it is dark, and a flint pick breaks it out, in four seconds: two to four lumps of sky iron.
  - **In the three nights before the Skyspear arrives a star falls near you every night,** and shooting stars come thicker each night as it nears: five a minute on the first night, 26 on the eleventh.
  - A star whose moment passes while you sleep does not fall. One whose moment the T key moves the clock past still falls, if it is night.
- **The Skyspear** is a comet, in the night sky from the first night: a bright head with a tail of light behind it.
  - **It grows each night.** On the first night it is a speck. By the eleventh its tail crosses a third of the sky.
  - **It is fixed among the stars and turns with them:** it rises at dusk lying along the horizon, stands upright at midnight, and sets at dawn. A near one shows through the dusk and the dawn, before the stars do. Ash hides it.
  - **It arrives at the midnight of night 12,** two hours of play, and a new one every 24 days after. On its last evening the low sky is red and its tail is the color of fire.
- **The Great Fall** is the night it arrives.
  - **For three minutes round midnight stars come down thick:** one every two seconds, anywhere within 96 blocks of you, each with its fireball, its flash, its boom and its crater. Two or three are in the sky at once, and the land is as bright as dusk all through.
  - **One can strike where you stand,** which a lone star never does: 12 points. Your bed keeps them off, by 24 blocks, and so do a pot and a hearth, by eight.
  - **Shelter is three blocks of earth or stone over your head:** a cave, a lava tube, a cellar. A star that strikes over you breaks the roof open and does not hurt you, and its core lies in your floor. Leaves and wood do not stop a star, and a hut on the ground is no shelter.
  - **Beasts run** from where a star strikes, from 40 blocks.
  - **Nobody sleeps that night:** a bed will not take you until it is over.
  - **Then the Skyspear itself strikes, far off.** The sky goes white for three seconds. Twenty seconds later its boom comes and the ground shakes hard for six. It does not hurt you.
  - **Ash climbs the sky** in the minute after, and stays for four days: the light of day is down by a third. Then it thins for half a day.
  - **It leaves the land round you full of craters,** dozens of them, each with its core of sky iron.
- **The Long Winter** is the four days after the Skyspear strikes. Then comes spring, and the next comet is a speck in the sky.
  - **Every land is cold,** as the steppe and the crags are at any time.
  - **The cold takes your warmth:** all of it in two minutes, with no fire and no furs. With none left you lose a point of health every four seconds, you do not mend however well fed, and the cold can make you faint.
  - **A fire gives it back,** all of it in 20 seconds, within six blocks: a fire, a hearth that burns, a torch that stands, lava, the hot core of a star. So does the water of a hot spring. Out of the cold it comes back by itself, in 40 seconds.
  - **A fur cloak** is four hides and two cords, made by hand. It works while you carry it: there is nowhere to put it on. With it you lose no warmth by day, and half as fast by night. So furs make the day safe, and the night still needs a fire.
  - **Frost whitens the open ground** and the tops of the trees, in the first minutes, and goes with the ash. It is paint: no block is changed, and under a roof or thick leaves the ground is as it was.
  - **Herds are thin:** half as many of the beasts that live in a land are about, but never fewer than go together.
  - **Hunters are bold:** the ashen day is no light to a quickclaw, so they come at noon as at midnight. A fire's light still holds them off.
- **Tools of obsidian** are knapped at a knapping stone, as flint is. They hit hardest and dig fastest, and are worn out after 40 uses, where flint on a handle lasts 130.
  - An obsidian knife (an obsidian, a stick and a cord) hits for 5 and carves a kill.
  - An obsidian pick (3 obsidian, 2 sticks and a cord) digs four times as fast as a hand, and breaks out crystal, as a sky iron pick does. The camps want crystal shards, and nothing is made of them.
  - An obsidian spear (an obsidian, 3 sticks and a cord) hits for 5, reaches a block farther, and takes 7 thrown.
- **Tools of sky iron** are hammered cold at a knapping stone. They are the strongest there are and last longest, 400 uses, where obsidian lasts 40.
  - A sky iron knife (a lump, a stick and a cord) hits for 6 and carves a kill.
  - A sky iron pick and a sky iron axe (3 lumps, 2 sticks and a cord each) work six times as fast as a hand.
  - A sky iron spear (a lump, 3 sticks and a cord) hits for 6, reaches a block farther, and takes 8 thrown.
  - The four tools take eight lumps, and a crater holds two to four.
- **A striker** is a flint and a firestone, made by hand. E with it on a hearth that has fuel lights it at once, where a fire drill takes six seconds. E with it anywhere else lights the first unlit torches you carry, with no fire near. It lasts 30 fires.

![A fire mountain at night from its foot, a dark cone with the red of its fire rising from the crater](docs/mountain.png)

![A hot spring at the foot of the cone, blue water in rings of rust, gold and green stone, with the white steam of its geyser going up](docs/spring.png)

![A fire mountain that erupts under a grey sky, with burning rocks coming down its side and the fire they trail](docs/eruption.png)

![A falling star over the tops of redwoods at night, a bright head with its tail behind it and a glow round it](docs/star.png)

![The Skyspear early in the night before it arrives: a comet low over the horizon, its bright head and a long tail of light among the stars](docs/comet.png)

![The Great Fall: a red sky over a forest lit as at dusk, a fireball coming down, and the fires of craters among the trees](docs/greatfall.png)

![The Long Winter from above the trees: frost white on the ground and on the tops of redwoods under a grey sky, with the warmth bar over the health](docs/winter.png)

- **Giants that stand their ground.** Three armed plant-eaters do not run from you. Each is few, strong and worth a great deal of meat, and each can be killed, with work. A giant is met by a spear or a hand all along its body, climbs a step of two blocks, and is too heavy for a hit to knock back.
  - **Shieldbrows** are horned, with a shield of bone behind the head, and go as a family on the prairie: two grown and one or two young. Come within ten blocks of a young one and a grown one turns on you, lowers its head and bellows. Come within six, or hit one of the family, and it charges at 7 blocks a second: 6 points, and you are thrown. It cannot turn fast, so something solid between you saves you. Then it goes back to its young. It charges a quickclaw the same way. 60 points of health, 8 pieces of meat and 3 hides.
  - **Thornbacks** carry plates along the back and four spikes on the tail, and go alone in the highland and the jungle. Within six blocks of one it rattles and turns its tail to you; within reach of the tail it strikes, every 1.6 seconds: 5 points, and you are thrown. 45 points of health, 6 pieces of meat and 2 hides.
  - **Boulderbacks** are low, slow and armored, with a club at the end of the tail, and go alone in the badlands. The armor takes 3 points off every hit: a hand or a stab does nothing, a club 1, a thrown spear 2 and a thrown hardened spear 3. The club strikes for 7. 50 points of health, 6 pieces of meat and 2 hides.

  - **Cloudgrazers** are the giants among them: a long neck that reaches 13 blocks up, a tail as long, 20 blocks from nose to tail. They go in pairs on the prairie and the shore, slowly, walk through the leaves of trees, and take no notice of you. One cannot be hurt and does not run: a spear thrown at it lies where it fell. Keep out from under it: a foot that comes down on you takes 8 points and throws you aside.
- **The coal swamp** is low wet country that the water has soaked flat, a step or two over the sea. It is about one part in 25 of the world.
  - **Its ground is peat,** black and wet. A digging stick digs it, and a piece burns in a hearth for 240 seconds, three times as long as a log. Coal lies in seams two blocks under the top of it.
  - **Its pools are black:** still water, one or two deep, that stands to the level of the sea, between banks of peat. Look for a sail before you wade into one.
  - **Scale trees** stand on the banks: a bare trunk 8 to 12 blocks tall, all diamonds where old leaves grew, with a small crown at the top. The trunk is a log like any other. One block of trunk in twelve also leaves a piece of amber. The camps want amber, and nothing is made of it.
  - Giant horsetails stand two and three blocks tall, with ferns and mushrooms between them.
  - **Rattlewings** are dragonflies as long as your arm, in ones and twos. They are the first thing that flies: one keeps a block and a half over the ground or the water, hangs in the air, darts off some new way, and never comes down. Its wings whirr. It does no harm. A hand's hit sends it off, and a spear's kills it.
  - **Logcrawlers** creep on the peat, alone: two blocks long, low, in red plates, on many legs. They do no harm and keep out of the water. Hit one and it curls up, both ends over its middle, for six seconds: curled, nothing hurts it. 8 points of health, 2 pieces of meat.
  - **Sunbacks** hunt the swamp and the badlands by day, alone, from noon of the second day: as long as you are tall, low, with a sail the color of fire on the back. **The sun warms one.** At noon it runs 6 blocks a second, faster than you walk. At sunrise and at sunset it has four tenths of that, and you walk away from it. It outruns you through the middle two thirds of the day. In the Long Winter there is no sun, and it is slow all day. In the dark it lies still. 35 points of health, a bite of 6, 4 pieces of meat and 2 hides.
  - **Sailjaws** lie in the pools of the swamp and in still shallows by the swamp and the jungle, one in a place: bigger than a sunback every way, with jaws as long as you are tall. One lies at the top of the water with its back under it, and **only its sail stands out.** Under the water it is a dim shape. From more than seven blocks it takes no notice of you. From the second night on, come within five and it lunges, out of the water if it must: 9 points. Two steps to a side save you from a lunge, and on land it is slower than you. It follows no more than ten blocks from where it lay, and then goes back to its water. 60 points of health, 6 pieces of meat and 3 hides.
- **Tar pits** lie in the swamp and the badlands, where the seed puts them: a round black pool six to ten blocks across and three deep, level with the ground, with the bones of what it caught standing out of it.
  - **Tar holds you.** In it you crawl, at a fifth of a walk, and you sink, 0.08 blocks a second, whatever you do: a jump does not lift you. Your head is under in about twenty seconds, and then your air goes as it does in water.
  - **At the edge you climb out:** walk into the bank and you go up it. From the middle of the widest pit that is six seconds of crawling.
  - **A beast is held for good.** Tar looks like ground to it. Once in, it goes nowhere, sinks, and dies there in a minute, however strong: lead a hunter across a pit, or drive a giant in. A beast that nothing kills, a mossback or a cloudgrazer, knows tar and keeps out of it. What flies goes over it.
  - **Tar comes away in the hand,** a block at a time, and can be put down again where you like. A stick and a piece of tar make two unlit torches, as a stick and resin do.
- **The sea has beasts of its own,** which swim. Each keeps to water deep enough for it, lies at the top of it or goes down in it, and never comes onto a bank. None is under ice.
  - **Lakenecks** lie far out, where the water is five deep or more, in twos and threes: a broad body just under the water, and a neck as long as the rest of it that stands up out of it. Their moan carries over the water. They are shy. Come within twelve blocks and they sink, three blocks down, and swim off faster than you swim. Left alone they come up again. 40 points of health, 6 pieces of meat and 2 hides.
  - **Leapfins** go in schools of four to seven, where the water is three deep or more: dark above and white under, with a long beak and a fin that cuts the water. Every few seconds one leaps clear of it. They do not fear you. Swim within 22 blocks of a school and it comes, and keeps by you as you swim. 6 points of health, 2 pieces of meat.
  - **The deepmaw** is the hunter of the deep: twelve blocks long, a quarter of it jaws, alone. It keeps to water six deep or more and lies three blocks down, a long shadow, until it has seen its prey: a lakeneck, a leapfin, or you, from 26 blocks, from the second night on. **Then its back breaks the water,** and it comes, at 7 blocks a second: 10 points a bite, half of all you have, and another every two and a half seconds.
  - **In the shallows you are safe.** A deepmaw goes for you only while you are in water six deep or more, and it does not come into less: it stops at the edge of the deep. Out of the water you are nothing to it. Shores, ponds and the pools of the swamp are too shallow for one. 160 points of health, 12 pieces of meat and 4 hides.
  - **Water is seen into, and not through.** What lies under it fades as it deepens, and ten blocks down it is gone. A beast in the water is a dim shape, and one that lies deep is not seen. With your eyes under water you see twenty blocks.
- **Two great beasts have wings.**
  - **Galewings** soar over the shore and the sea, in ones and twos: a small body between wings eight blocks from tip to tip, a long beak and a red crest. One turns in a circle 14 blocks over what is under it, then in another, and keeps by the place it was first seen. Over water it comes down now and then and skims it. Its cry falls from high up, and carries. It takes no notice of you. 12 points of health, 2 pieces of meat, if your spear reaches one.
  - **At night a galewing sleeps on high ground:** bare ground or rock that stands six blocks or more over what it soars over, within forty blocks, with its wings folded. At sunrise it flies. Where there is no such ground it soars all night.
  - **From far off the sky draws them:** a galewing beyond your view distance is a small dark shape of two wings over the horizon, as far as 104 blocks.
  - **Stiltwings** stalk the badlands on foot, in ones and twos: a body two blocks up on four stilts, of which the front two are its folded wings, a neck as high again, and a head that is nearly all beak. They are as tall as a tree, and clatter their beaks. Come within fourteen blocks and one takes to its wings: it climbs to ten blocks over the ground, flies off far faster than you walk, and comes down some sixty blocks away, where there is ground to stand on. It does no harm. 25 points of health, 4 pieces of meat and a hide.
- **Nests and eggs.** Some herds keep a nest: a ring of dry grass on the ground with one or two eggs in it. Which herd does is the seed's choice.
  - **One bugler herd in three** has one, where the herd stands. **One shieldbrow family in two** has one. **A pair of galewings** has one on high ground within forty blocks of where it soars, if there is any, and that is where the pair sleeps.
  - **Q or E takes an egg** you aim at, from as far as your hand reaches. It goes into your bag: a bugler's egg, a shieldbrow's or a galewing's. It is no food, and it keeps.
  - **Buglers run at a thief.** For eight seconds the grown ones of the herd do not run from you: they run you down, 3 points each time one meets you. Their young keep back. Then they are a herd again.
  - **Shieldbrows guard an egg as they guard their young:** they warn you ten blocks from it and charge you six blocks from it. Take it, and every grown one of the family charges: 6 points.
  - **Galewings dive at you** while you are within twenty blocks of their nest, by day: straight down at your head, 2 points a pass, each no more than once in six seconds.
  - A nest you leave far behind is gone with its herd.
- **Raising a beast.** There is no knocking out and no waiting on a bar: an egg, a fire, and two meals.
  - **E with an egg in hand puts it down** on the ground you aim at. Q or E takes it up again.
  - **By a fire it hatches.** An egg within six blocks of a fire gathers warmth, and ten minutes of it, one day of the world, hatch it. A hearth that burns warms it wherever you are, so stock the hearth and go: a day is eight logs, or three pieces of peat. Any other fire warms it only while you are within twelve blocks. Away from a fire it keeps the warmth it has.
  - **What hatches is yours:** half the size of a grown one, and it follows you, as a tame mossback does.
  - **A meal from your hand is a day of growing.** Berries, fruit or fiber for a bugler and a shieldbrow, raw meat for a galewing. It takes no other meal while that day lasts. After two days of growing it is grown. Unfed it does not grow, and it does not starve.
  - A young galewing goes on foot until it is grown.
  - **A beast of yours does not die.** One that loses all its health limps home, at half a walk: to your bed, or with no bed to where you first stood. Nothing hurts it or hunts it on the way, and it takes no food. A day after it fell it is whole.
  - A shieldbrow of yours does not turn on you, and a beast of yours keeps out of tar.
- **Riding a bugler.** E on a grown bugler of yours gets you on its back, and C gets you down beside it, where there is room.
  - **W A S D ride it** the way you face. W sets it off at your walk, and held it gathers speed for a second and a half to a run of 9 blocks a second, twice your walk. S backs it. A and D turn it, as the arrows do. Space jumps: it clears two blocks, and it hops a step of one by itself.
  - **You see from its back,** through your eyes over its lowered head, or from behind. It carries its head low and forward while you ride.
  - **What hits you hits you.** Hunters still come, but at a run you leave every one behind but the daggercat's spring. A fall is the bugler's, as for a heavy beast: two blocks and no more is no harm, and a jump is no fall.
  - A young bugler is too small to ride, and one that limps goes home. One that loses all its health while you ride it throws you off. You get down to throw.
- **Riding a shieldbrow.** E gets you on a grown shieldbrow of yours, as on a bugler. You see over its shield of bone.
  - **It is slow and strong:** it walks at 3 blocks a second, W held or not, and nothing knocks it back.
  - **Space charges:** two seconds at 8 blocks a second, head down, the way you face. The first hunter its head meets takes 7 points and is thrown back, and that ends the charge. Then it rests four seconds before it charges again. It does not ram the dread, and the dread hunts it as before.
  - **A hunter that one charge would kill keeps off you,** ten blocks off, while you ride a shieldbrow. None has so little health until it is hurt: a quickclaw or a howler you have charged once keeps off after that.
- **A snowtusk calf.** A snowtusk is not hatched: you win a young one from its family, with food.
  - **Crouch, with food it eats in your hand:** fiber, berries or fruit. Then the family lets you come to the calf. Stand up, or come with anything else in hand, and they warn you and charge, as before.
  - **E feeds it from your hand.** Five meals and it is yours, but it takes no more than three in a day: three one day and two the next win it. A grown snowtusk eats nothing from your hand.
  - **Then it leaves its family** and follows you, and its family lets it go. It grows as a young beast you hatched does: a meal a day, two days of growing.
  - **Ride it grown,** with E. It is the slowest of your mounts and the hardest to stop: it walks at 2.5 blocks a second, W held or not, and pushes through leaves. A hunter in its way is run down: 7 points, and thrown aside. It does not run down the dread.
  - **On its back you keep warm.** The cold of the steppe and of the Long Winter takes none of your warmth while you ride it.
- **A galewing's glide.** A galewing you raised is not ridden: it carries you down from high places.
  - **Grown, it keeps over you** by day: it circles where you are, and comes straight back when you leave it twenty blocks behind. At night it sleeps on high ground near your bed, where there is any.
  - **Step off a height with it near and it takes you.** Six blocks or more must be under you, with open sky over you, and the galewing in the air within 32 blocks. It holds you by the head and you glide: 9 blocks a second ahead, and a block down for every five. From a mountain you cross a valley.
  - **A and D turn you, W dives,** a block down for every two, and **C lets go:** you fall from there, and it does not take you again until you are down. W held as you step off does not dive: let it go and press it again. It cannot climb: a glide starts high and ends low.
  - **It sets you down unhurt,** on the ground or in water, and takes to the air again. A wall does not end a glide: you go down along it.
- **The steppe** is the cold land: snow, tussocks of dry grass through it, and a few trees no taller than five blocks. It takes your warmth at any time of the world. Its beasts stand on the snow.
  - **Snowtusks** go in herds of three to five: three grown, five blocks tall, in long red hair, with a trunk and two tusks, and their young between them. Come within ten blocks of a young one and the grown ones turn on you, lower their heads and trumpet. Come within six, or hit one of the herd, and they charge, together: 7 points each, and you are thrown. 80 points of health, 10 pieces of meat, 4 hides, which is a fur cloak, and from a grown one two tusks. The camps want tusks, and nothing is made of them.
  - **Slowclaws** go alone, slow and shaggy, with long arms that end in claws. One takes no notice of you, however near. When it stops it stands up on its hind legs, three blocks tall, as it does to feed from a tree. Hit it and it stands up and comes at where you were, slowly: 6 points. Step away and it does not follow. 40 points of health, 6 pieces of meat and 3 hides.
  - **Howlers** hunt the steppe by night, in packs of four to six, from the second night. They come only to one who is on the steppe. You hear the howl first, from 48 blocks off, and eight seconds later the pack comes out where it howled. They are quicker than quickclaws and more of them: 12 points of health each, a bite of 3. They hunt the herds as well as you. Light holds them off, as it does quickclaws: a torch in your hand is enough.
  - **The daggercat** lives on the steppe, one in a place, and hunts by day. It sees you from 26 blocks, runs to within 16, and comes on from there at a walk, low. From eight blocks it snarls and springs, faster than you can run: 7 points, a third of all you have. Then it backs off for three seconds and comes again. A spring goes where you stood when it began, so two steps to a side save you. It lies still in the dark. It will not come within twelve blocks of you while you are by a fire. 30 points of health, 3 pieces of meat and 2 hides.
- **The ground shakes.** Each step of a cloudgrazer is a thud heard from 90 blocks off, and within 40 your view shakes with it: a little from far, hard from five blocks. `Ground shake` in the settings turns the shaking off and leaves the sound.

![Two cloudgrazers by a pond, their necks up among the leaves of the trees, with a cave person before them](docs/cloudgrazers.png)

![A herd of snowtusks on the snow of the steppe: two grown ones in long hair, with trunks and tusks, and a young one between them](docs/steppe.png)

![Two howlers on the snow by day: grey, long in the leg, with ears that stand and pale eyes](docs/howlers.png)

![The coal swamp from above: black pools winding between banks of peat, giant horsetails, and scale trees with their crowns at the top of bare trunks](docs/swamp.png)

![A tar pit in the red badlands, black, with bones standing out of it, and the dread sunk in it to its back](docs/tar.png)

![Two lakenecks at sea: long necks with small heads standing up out of the water, and the dim shapes of their bodies under it](docs/lakenecks.png)

![A school of leapfins: two in the air over the water, dark above and white under, and the fin of a third cutting the water](docs/leapfins.png)

![A cave person riding a bugler on the snow of the steppe, sitting behind its neck, its head carried low and forward](docs/ride.png)

![A cave person riding a shieldbrow on the sand, sitting high on its broad back behind its lowered head and its shield of bone](docs/ride-shieldbrow.png)

![On the snow of the steppe, seen low from where a cave person crouches with berries in hand: two grown snowtusks, and their calf between them](docs/calf.png)

![A cave person riding a snowtusk on the snow, small on the top of its back over its shoulders, by its trunk and tusks](docs/ride-snowtusk.png)

![A cave person in a glide high over the snow, seen from ahead, held by the head by a galewing with its long wings spread](docs/glide.png)

![A fire on the prairie with two eggs by it, and beside it a young shieldbrow and a young bugler, each half the size of a grown one](docs/hatch.png)

![A nest on the prairie: a ring of dry grass with two pale eggs in it, and three buglers standing behind it](docs/nest.png)

![Two galewings in the air over the sea: pale, with long wings, a yellow beak and a red crest](docs/galewings.png)

![Two stiltwings on the red ground of the badlands: tall on thin legs, each with a long neck and a head that is nearly all beak](docs/stiltwings.png)

![A deepmaw at the top of the sea: its black back out of the water, and the long shape of the rest of it under](docs/deepmaw.png)

![A black pool of the swamp with the grey sail of a sailjaw standing out of it and the dim shape of its body under the water, and on the bank a sunback with a sail the color of fire](docs/sails.png)

![A thornback under a jungle tree, with rust red plates along its back and spikes on its tail](docs/thornback.png)

- **Throwing.** R throws the spear in your hand the way you aim. It leaves at 24 blocks a second and falls as it flies, so it comes down some ten blocks off thrown level, and 36 at the most; aim up for a far throw. It takes 2 points more from a beast than a stab does, 5 for a spear and 6 for a hardened one, and the beast's herd runs. A spear that misses sticks in the block it meets, pointing as it flew, until you walk up and take it; one that hits lies by the beast. A throw is a use, and a spear on its last breaks where it lands.
- **A sling** throws a pebble of those you carry, at 38 blocks a second, about every half second while R is held: 100 blocks at the most. A pebble takes 2 points, and a herd takes alarm when one lands within eight blocks of it, hit or not, so a herd can be driven from far off. The pebble lies where it landed. A sling lasts 80 shots.
- **Meat.** A beast that dies sinks, fades and leaves raw meat: a bugler three pieces. Raw meat is food, 5 points a piece, and 12 once a hearth has cooked it.

![A tree that lightning struck, burning at its top and at its foot in the night, with its smoke rising](docs/fire.png)

![A herd of buglers on the fern prairie, seen through a stand of horsetails](docs/herd.png)

- **Quickclaws** are feathered hunters as tall as you, in packs of two or three, in survival only. They come out where it is dark, at night under the sky or in a cave, 16 to 36 blocks from you, and they go when the day comes. The first night of a world is quiet: they come from the second.
  - They run a little faster than you walk, so you cannot outrun one. A bite takes 3 points, once a second.
  - **Light holds them.** A quickclaw will not step into light: it stops about four blocks from a torch, in your hand or set down, or from a hearth that burns, and waits, and its eyes shine in the dark.
  - They hunt the herds too. With no player to go for, a quickclaw goes for the nearest beast within 16 blocks that can be killed and does not hunt, and stands over a kill for a quarter of a minute. The meat is there for whoever takes it.
  - A quickclaw has 10 points of health, so a sky iron knife kills it in two hits. A hit only sets it back for a moment, unless it is badly hurt with none of its pack within ten blocks: then it runs.
  - Quickclaws are not saved, and they lose you when you faint or sleep.
![A cave person by a torch at night, with two pairs of shining eyes in the dark beyond its light](docs/night.png)

- **The dread** is the top hunter: five blocks tall and nine long, with jaws as long as you are. It is in survival only.
  - **It comes rarely, and you feel it first.** None comes before the morning of the third day. Then one comes at a time, by day or night, 70 to 86 blocks off, and the next comes a day or two after the last has gone. Its steps are heard from 90 blocks and shake your view from 60, and it roars when it has noticed you.
  - **You cannot outrun it or fight it in the open.** It runs at 6 blocks a second against your 4.3, a bite takes 8 of your 20 points, once every second and a half, and it has 200 points of health, which is 34 thrown hardened spears. It sees you from 40 blocks and hears you move from 28.
  - **You hide, or go where it cannot.** Crouched among tall ferns or horsetails it sees you only from 3 blocks, as a quickclaw does. Its body is over two blocks wide, so it cannot follow through a gap of two blocks or into a narrow cave.
  - **Only a big fire holds it.** It walks through the light of a torch or a hearth. Three or more fires burning within four blocks of each other, hearths, standing torches or a struck tree's fire, are a big fire, and it will not come within seven blocks of one.
  - **It hunts the herds.** With no player noticed it goes for the nearest beast within 32 blocks, giants too, and stands over a kill for 20 seconds. Quickclaws within 16 blocks of it run.
  - It is about for half a day, and then goes. It is not saved, and it loses you when you faint or sleep.

![The dread at dusk among a herd by the shore, its eye shining, with the neck of a cloudgrazer against the sky](docs/dread.png)

- **Pit traps.** A pit cover is a block of branches and ferns that you lay over a hole as you lay any block. It holds you, a nipper, a mossback and a quickclaw. A bugler, a giant or the dread that gets its middle onto one breaks through: the whole cover gives way at once, and the beast is tipped in.
  - **The fall hurts a heavy beast:** nothing for two blocks, then a sixth of its kind's health for each block more. A pit four deep takes a third of a dread's 200 points, and a third of a bugler's 16.
  - **It cannot climb out:** a giant climbs two blocks and a bugler one. From the rim you throw spears down, or stab: a dread in a pit four deep cannot reach you, and its head stands just over the rim.
  - **This is how the dread is killed.** It leaves 12 pieces of meat and 4 hides. Dig the pit three wide each way, as it is over two blocks wide, cover it with nine covers, and have it come at you across it.
- **Stampedes.** A herd that runs in alarm runs down what is in its way: you, as before, and now every lighter beast of another kind, for the 3 points a bugler's bump takes. A pebble from the sling makes a herd run from where it lands, so a herd can be driven over a pack of quickclaws, or into your pit.

![A pit covered with branches and ferns in the moss, and the dread coming toward it](docs/pit.png)

- **Hiding.** A quickclaw sees you from 20 blocks, from 10 if you crouch, and from 3 if you crouch among tall ferns or horsetails, and never through a wall. It hears you move from 14 blocks, and from 3 if you crouch. Raw meat anywhere on you doubles all of these. The line at the top of the screen says `hidden` when you are, and one that has lost you keeps looking for six seconds.
- **Fainting.** At no health you faint, and wake at your fur bed or where a new player starts, whole again and with everything you carried.
- **Creative.** Every block on the I screen, as many as you want, broken at once and dropping nothing. Nothing hurts and you can fly.
- These numbers are first guesses, to be tuned.

- A day lasts ten minutes of play, and the clock stands still in a pause. A new world starts in the morning.

## Worlds and saving

The title lists your worlds, the last played first, with how each is played and its day. Choose one to play it, or to delete it: that asks twice, and a deleted world is gone for good. **New world** asks for a name, then a seed (leave it empty for any), then how it is played.

The world is saved when you choose **Save and leave**, which goes back to the list, and also on **Quit**, Ctrl-C or when the window closes.

- A world is a folder of `skyspear/worlds` in your config folder (`~/Library/Application Support` on macOS, `~/.config` on Linux), named as you named the world; `-worlds` names another folder of worlds. It holds `world.json` (the seed, the mode, the day and the hour, where you were, what you carry, how your body is, what lies on the ground, what the pots and the hearths hold, your bed, the look you wear, how far the torch in your hand has burned, your paintings, what you have met, how much each camp trusts you, your fire, and who came to live at it) and one small file for each chunk you changed. The rest of the world is made again from the seed.
- Every file is written beside the old one and then put in its place, so a write that fails leaves the old file.
- A world whose `world.json` cannot be read is listed as such and does not open, so it is never written over. It can still be deleted.
- `-world folder` plays the one world in that folder, with no list, as the game did before: the title offers **Continue**, **New world** asks before it takes the place of the saved world, and a `world.json` there that cannot be read stops the game with an error.
- A chunk file that cannot be read does not stop the game. The chunk is made again from the seed, a line on screen says so, and the file is never written over, so what you build in that chunk is not kept.
- **A world made with v1.0.0 or later** opens in every later release.
- **A world saved before the land turned old** (by `v0.2.0` or earlier) is listed as from an older version and does not open: some of its blocks are now other things. It is left untouched, and the game that made it still installs from its tag.
- **Worlds made under the old name** are still in `gocraft/worlds` in your config folder, untouched. `skyspear -worlds` with that folder lists them, as from an older version.
- **The one world of the first version** (`gocraft/world.sav`) cannot be played by this one. It is left where it is, untouched.
- The people of the camps are not saved: they are made again from the seed when you come near. Those who came to your fire are saved, wherever they are.
- The beasts are saved: what kind each is, where it stood, its herd and its health, and a mossback's moss, shorn or grown.

## Settings

**Settings**, on the title and the pause menu, has the mouse speed (how far a drag turns the view), the view distance (32, 48 or 64 blocks: less is a little faster), the field of view (50° to 90°) the volume (0% to 100%), and whether the view shakes at a giant's step. Left and Right, or a click, change a line. They are kept in `skyspear/settings.json` in your config folder, apart from any world, and so is the view you last chose with V.

## Flags

| Flag | Meaning |
|---|---|
| `-seed n` | the number a new world is made from, offered as its seed; the same number makes the same world. 0, the default, takes one from the clock |
| `-worlds folder` | the folder of the worlds the title lists |
| `-world folder` | play only the world in this folder, with no list |
| `-mouse=false` | leave the pointer to the terminal |
| `-mute` | play with no sound, and leave the sound device alone |
| `-shot file.png` | draw one frame of play into a PNG and quit, to look at it without a terminal. A letter is a mark in its color where it stands |
| `-version` | print the version and quit |

## In a web page

The same game plays in a web page, on [its page](https://usr.games/skyspear) at usr.games. In a page:

- **Nothing is kept.** A page has no folders, so each visit begins a new world, and the settings start as they do the first time. The title says so, and the pause menu says Quit.
- **The sound starts at the first key or click,** as browsers ask.
- **The flags do not apply,** and the mouse is always the game's.

## License

You may download Skyspear, install it and play it, free of charge; [LICENSE](LICENSE) is the whole of what it allows. [NOTICES](NOTICES) holds the licences of Go and of the modules the game is built from.
