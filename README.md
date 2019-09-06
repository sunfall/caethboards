# caethboards

This repository contains various artisanal, hand-crafted Caeth, Noc, and Noeth
boards of many sizes and styles for your board game playing enjoyment.  (Or
adult coloring, thanks to the hypnotic repeating patterns.)

These boards are released into the public domain and are best played with
colored pencils, preferably four in two sets of related shades.  Give each
player one of the sets, and have them use one color for the undergame voting
cells and the other for the won overgame cells when successfully claimed.

Alternately, using the _flood fill_ or _paint bucket_ tool in most paint
programs will work as a way to play with these boards on the computer, whether
via PBeM or Google Drive or what have you.

Pre-rendered American letter-sized versions are in the `pdf/` directory.  The
Inkscape source SVGs are in `src/`.

# The metarules

All of the metarules used by these boards are voting or majority "mutators"
that you can use to modify a number of different board games (hereafter the
*overgames*); they work best with connection games, and in particular ones
where pieces are placed on the board and never moved or removed afterwards,
although they can be modified to handle piece removal.

## Caeth

With the Caeth metarule, every pair of adjacent cells has an edge (or _node_)
between them as part of the Caeth *undergame*.  Players take turns claiming one
of those nodes per turn; use the pie rule for the first move.  An overgame cell
is immediately claimed by a player when that player controls half or more of
the Caeth nodes into that cell; a single node may trigger more than one
overgame cell claim at the same time.

A player wins a Caeth metarule game _only by winning the overgame by its
standard win condition (connecting both sides, all three sides, etc.)_,
counting **only** the overgame cells.  The undergame nodes are not considered
part of any overgame connection.

## Noc

The Noc metarule is similar to the Caeth metarule, except the undergame
involves nodes that lie at the adjoining or "meeting points" of the cells of
the grid.  In a hexagonal tiling, that means most Noc nodes are votes for three
cells rather than just two.  It is named in honor of ConHex, which uses a
custom board but a closely-related version of this mechanism.

## Noeth

Noeth is a combination of both Noc and Caeth, with the undergame nodes for both
on the same grid.  It uses a modified 1-2-2-2... move protocol; the first
player fills in any undergame node, and from then on each player fills in two
undergame nodes _if and only if_ they are one Noc node and one Caeth node *and*
those two choices do not share any overgame cells.  If they cannot meet those
criteria, or for some reason wish not to do so (possible in a game like
Havannah), they instead claim any single undergame node.

## Near-Noeth

Near-Noeth is identical to Noeth, except that the criteria for dual claiming is
as follows: you fill in two undergame node _if and only if_ they are one Noc
node and one Caeth node *and* those two choices share **precisely one**
overgame cell.  As in standard Noeth, an inability to do so (or a choice not
to) results in claiming a single undergame node.

# The boards themselves

The boards are named based on which metarule they're meant for (`caeth-`,
`noc-`, or `noeth-`), and then come in various sizes and variants:

* `-hex-`: Boards meant for Hex and any variants played on the same board.
* `-hexhex-`: Boards meant for any game that uses a regular hex-hex board.
* `-square-`: Boards meant for games on a square grid.
  * `-4square`: A Caeth-specific version with explicit orthogonal votes.
  * `-8square`: As `4square`, but with added diagonal votes.
* `-y-`: Boards meant for the Game of Y.

The `caeth_loz-` boards are a variant art-style for Caeth boards that makes the
overgame cells much more prominent, much like the Noc and Noeth designs.

# Sizes and numbers

For a given overgame, there are usually several boards of different sizes.  In
addition, the PDFs are rendered two different ways for each board: one with
light grey numbers representing the number of undergame nodes needed to claim a
given cell, and one without those numbers; the latter have a `-no-counts`
suffix.

Some boards are small enough that multiple copies are present on the same page
in the printable PDFs.

# Using these elsewhere

If you want to use these as a base for further works, you'll want to use the
`-unscaled` versions as your base.  They're still grid-aligned, which makes
editing them much easier than the formatted-for-printing files.  (I'd also
appreciate a heads-up as to what you're using them for, but that's obviously
not required.  Just, y'know, appreciated.  My email address is phil PERIOD
bordelon SWIRLY-A gmail FULLSTOP com, with the appropriate substitutions.)

Also feel free to contact me if you're interested in a PBeM (or equivalent)
game with one of these boards.  Or if you color then in a particularly pretty
fashion.
