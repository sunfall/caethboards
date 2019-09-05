# caethboards

Caeth, Noc, and Noeth boards of various sizes for playing different connection
games.

These boards are released into the public domain and are best played with
colored pencils, preferably four in two sets of related shades, one for the
voting edges or points and one for the cells themselves.

Pre-rendered American letter-sized versions are in the `pdf/` directory.  The
Inkscape source SVGs are in `src/`.

# The metarules

## Caeth

Caeth is a voting/majority metarule that you can use to modify a number of
games (hereafter the *overgame*); it works best with connection games, and in
particular ones where pieces are placed on the board and never moved or removed
afterwards.

In the Caeth metarule version of a game, each adjacent cell has an edge between
them as part of the Caeth *undergame*.  Players take turns shading one of those
edges per turn; use the pie rule for the first move.  When any overgame cell
has half or more of its edges claimed by a single player, it is claimed by that
player.  A player wins by winning the overgame by its standard win condition
(connecting both sides, all three sides, etc.), counting _only_ the overgame
cells.  The edges are not considered part of any connection.

## Noc

The Noc metarule is similar to the Caeth metarule, except the undergame
involves cells rather than edges that lie at the adjoining or "meeting points"
of the cells of the grid.  In a hexagonal tiling, that means most Noc cells
count for three cells rather than just two.  It is named in honor of ConHex,
which uses a custom board but a closely-related version of this mechanism.

## Noeth

Noeth is a combination of both Noc and Caeth, with the nodes for both on the
same grid.  It uses a modified 1-2-2-2... move protocol; the first player
fills in any node, and from then on each player fills in two nodes if and
only if they are one Noc node and one Caeth node *and* they do not share
any overgame cells.  If they cannot meet those criteria, they instead fill
in any single node.

# The layouts

The boards are named based on which metarule they're meant for, and then come
in various sizes and variants:

* `-4square-`: Boards meant for games on a square grid; votes are orthogonal.
* `-8square-`: As `4square`, but with added diagonal votes.
* `-hex-`: Boards meant for Hex and any variants played on the same board.
* `-hexhex-`: Boards meant for any game that uses a regular hex-hex board.
* `-y-`: Boards meant for the Game of Y.

# The sizes and variants

For a given overgame, there are usually several boards of different sizes.  In
addition, the PDFs are rendered two different ways for each board: one with
light grey numbers representing the number of undergame nodes needed to claim a
given cell, and one without those numbers.

Some boards are small enough that multiple copies are present on the same page
in the PDF.

# Using these elsewhere

If you want to use these as a base for further works, you'll want to use the
`-unscaled` versions as your base.  They're still grid-aligned, which makes
editing them much easier than the formatted-for-printing files.  (I'd also
appreciate a heads-up as to what you're using them for, but that's obviously
not required.  Just, y'know, appreciated.  My email address is phil PERIOD
bordelon SWIRLY-A gmail FULLSTOP com, with the appropriate substitutions.)
