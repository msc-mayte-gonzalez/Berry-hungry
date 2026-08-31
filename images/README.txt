Play-screen background + player + intro credits + rescue progress +
ground rocks + hearts + win helicopter — ten image files

Drop files into this folder with these exact names. Nothing else
needs to change in the code -- each one lights up automatically as
soon as it's here.

  background.jpg   The full-screen forest scene the player "walks"
                    through -- fills the whole play screen behind
                    the plants and the ground path.

  player.png        The first-person player art (hands/torso, or
                    whatever the character design ends up being) --
                    anchored to the bottom-center of the screen, on
                    top of the background and stage.

  credits.png       The image shown on the very first "credits"
                    screen, before the Berry Hungry title screen --
                    only appears once, on first load. See below.

  rescue-marker.png  The small token that climbs the rescue-progress
                    track in the upper right of the HUD as the player
                    picks correct plants -- see below.

  rescue-goal.png    The helicopter icon fixed at the TOP of that
                    same track -- the thing the marker is climbing
                    toward. See below.

  rock-small.png     The smaller of two decorative rocks scattered
                    along the walking trail, moving toward the
                    player as they walk. See below.

  rock-big.png       The larger of the two decorative rocks. Same
                    placement behavior as rock-small.png, just a
                    bigger silhouette. See below.

  heart-full.png     A full/uninjured heart -- shown in the HUD
                    (upper left) and above the encounter cards for
                    each life the player still has. See below.

  heart-broken.png   The same heart, broken -- shown in place of
                    heart-full.png for each life the player has
                    already lost. See below.

  helicopter.png     ALREADY INCLUDED as a starter/placeholder --
                    the rescue helicopter that descends from the top
                    of the screen once the player wins. Swap it out
                    for final art any time by replacing this file
                    with a new one under the same name. See below.

Specs:

  background.jpg
  - Format: JPG
  - Resolution: around 1920x1080 (16:9) is a good target -- sharp
    on a normal desktop screen without being a huge download.
  - The image gets cropped to fill the screen on very different
    window shapes (tall phone vs. wide desktop), so keep the
    important stuff -- horizon, tree canopy, the trail -- roughly
    centered rather than close to the edges.

  player.png
  - Format: PNG with a transparent background (the shape of the
    art itself is what shows -- no rectangle around it).
  - The image sits in a box roughly 460px wide and about a third of
    the screen tall, anchored to the bottom, and is scaled to fit
    inside that box without cropping or stretching -- so an image
    around 900x700px (roughly the same proportions, a bit taller
    than wide) is a safe target. It'll scale down cleanly from
    there.
  - Keep the "grounded" edge (feet, base, whatever touches the
    ground) at the very bottom of the image -- that's what lines up
    with the bottom of the screen.

  credits.png
  - Format: PNG with a transparent background -- it sits centered
    over a solid black screen, so anything transparent in the image
    just shows black through it.
  - Scaled to fit inside a box up to about 39% of the screen's width
    and height, without cropping or stretching, so any reasonable
    size/aspect ratio works -- something in the 1200-2000px range on
    its longest side is a safe target (it'll just render smaller on
    screen than that box, same as before -- the source file doesn't
    need to be any smaller).
  - Shown once, automatically, only the very first time the page is
    opened -- never again on Start Over / Play Again / Try Again.
    The logo softly fades in (0.6s), holds fully visible (1s), then
    softly fades back out (0.6s), holds a silent black for a brief
    pause (0.3s), then the whole screen softly fades itself away too
    (0.6s) -- so the reveal isn't an abrupt cut -- into the Berry
    Hungry title screen underneath. About 3.1 seconds total.
    Clicking anywhere on it skips straight ahead, for faster
    playtesting.

  rescue-marker.png
  - Format: PNG with a transparent background.
  - Shows inside a ~56x56px circle, so it's cropped to a circle
    automatically (object-fit: cover would be more accurate, but this
    uses contain -- so a square or roughly-circular source with the
    subject filling most of the frame looks best; a source around
    300-500px square is a safe target). This is meant to read as "the
    player, in miniature" -- doesn't need to be a literal match to
    player.png, just recognizably the same character/idea.

  rescue-goal.png
  - Format: PNG with a transparent background.
  - Scaled to fit inside a ~80x80px box, so keep the silhouette
    simple and readable at a glance (a helicopter side-profile or
    similar) rather than detailed -- a source around 300-500px on its
    longest side is a safe target.

  rock-small.png / rock-big.png
  - Format: PNG with a transparent background.
  - rock-small.png is scaled to fit inside a box about 56x38px;
    rock-big.png inside a box about 108x70px -- both use "contain"
    (no cropping/stretching), so keep each source at roughly that
    same wide/flat aspect ratio (a rock lying on its side, not
    upright) with the subject filling most of the frame. A source
    around 400-600px on its longest side is a safe target for
    either.
  - These are scattered randomly and repeatedly along the ground the
    whole walk, moving straight toward the player (not diagonally
    outward like the trail plants), so keep them looking natural
    from a top-down "lying on the trail" angle rather than a
    dramatic side-lit hero shot -- they're background texture, not a
    focal point.

  heart-full.png / heart-broken.png
  - Format: PNG with a transparent background.
  - Each shows inside a square box that scales with the heart size
    used at that spot (a large ~54px box in the HUD/encounter modal
    on desktop, smaller on a narrow phone width) using "contain", so
    a simple square icon-style source works best -- around 300-500px
    square is a safe target for either.
  - Two SEPARATE files, not one image that gets recolored -- draw
    heart-broken.png as its own distinct art (a visibly cracked/split
    heart), not just a duller version of heart-full.png, since the
    game also applies a grayscale filter on top of whichever one is
    showing for a lost life.
  - Same two files are reused in both places hearts show (the HUD,
    upper left, and the small pair shown above the cards while
    picking) -- no separate versions needed for each spot.

  helicopter.png
  - Format: PNG with a transparent background.
  - Scaled to fit inside a box up to about 30% of the screen's width
    (max 170px), using "contain", so a roughly-square or wide source
    with the subject filling most of the frame works best -- around
    500-800px on its longest side is a safe target.
  - Descends straight down from off the top of the screen to just
    above the horizon line over about 2.2 seconds once the player
    wins, then the screen hands off to the "Rescued!" screen -- so a
    clear, readable silhouette from a slight top-down angle (as if
    glimpsed arriving overhead) works better than a straight side
    profile.
  - This one's already dropped in for you (using the placeholder art
    you shared) -- everything above just explains what a final
    replacement should match if you swap it out later.

Until these files exist:
  - background.jpg / player.png just show plain gradient/placeholder
    shapes in their place -- nothing breaks, it just looks unfinished.
  - credits.png shows a plain black screen with a small "credits --
    drop images/credits.png in to show it here" tag in the corner,
    then still fades into the title screen on the same schedule --
    so you can playtest the timing before the final art exists.
  - rescue-marker.png / rescue-goal.png each show as a small amber
    square with a "?" -- same placeholder language as the trail
    plants -- and the progress track/label still work and update
    normally in the meantime.
  - rock-small.png / rock-big.png each show as a simple gray drawn
    pebble shape in their place -- nothing breaks, it just looks
    like a placeholder rock instead of real art.
  - heart-full.png / heart-broken.png each fall back to the plain ♥
    / 💔 text characters (same red/gray look as before) -- the HUD
    and hearts-remaining count keep working normally in the meantime.
  - helicopter.png doesn't apply here -- it's already included (see
    above).

You can delete this file once all ten images are in place (nine of
them, anyway -- helicopter.png is already here).
