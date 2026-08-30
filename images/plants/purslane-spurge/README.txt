Purslane / Spotted Spurge — trail art (1 file)

This folder is different from the Purslane and Spotted Spurge
folders next to it -- those hold the identification-card photos for
each specific plant. This one holds the single image shown on the
WALKING TRAIL, before the player has tapped it and found out which
of the two look-alikes it actually is.

  walk.png   The plant as it appears on the trail while walking --
             shown in place of the amber "?" placeholder square.
             Lights up automatically as soon as it's here, no code
             changes needed.

Specs:
  - Format: PNG with a transparent background (the shape of the
    plant itself is what shows -- no rectangle around it).
  - Since this ONE image is shown for both encounters of this pair
    (the player doesn't know yet whether it'll turn out to be the
    Purslane or the Spurge), draw something that reads as "a low,
    ground-hugging mat of small leaves" in general -- close enough
    that it doesn't spoil which specific one it is, similar to how
    both plants already look enough alike to trick a forager.
  - Scaled to fit inside roughly a 64x64px box (small -- these sit
    scattered along the trail, not front and center), so keep the
    silhouette simple and readable at a glance rather than
    detailed. A source image in the 300-600px range on its longest
    side is a safe target.

Until this file exists, the trail still shows the amber "?" square
placeholder -- nothing breaks. You can delete this file once
walk.png is in place.
