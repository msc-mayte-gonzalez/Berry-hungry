Background music — two files

Drop files into this folder (music/, same level as images/ and
sounds/) with these exact names. Nothing else needs to change in
the code -- each one plays automatically, looping, as soon as it's
here.

  walk.mp3     Plays while the player is out on the trail (walking
               around, before tapping any plant). Starts the moment
               the Berry Hungry start screen appears (right as the
               credits fade away, whether that happens on its own or
               by clicking to skip), and again on "Try Again."

  choice.mp3   Plays instead, while the "which plant would you eat?"
               card screen is open -- swaps in the instant a plant
               is tapped, and swaps back to walk.mp3 the instant
               that screen closes (whether by picking a card, or by
               hitting the × to back out without choosing).

Both loop automatically for as long as their screen is showing, so
pick something meant to repeat seamlessly (a few bars to maybe a
minute is normal -- it'll just loop back to the start). Pausing the
game (the Pause button) pauses whichever one is currently playing,
and Resume picks the same one back up -- Start Over / Game Over /
Win stop all music, since none of those screens have their own
track.

Format: MP3 -- every current major browser plays it natively, no
conversion needed if that's already the format you have it in.
(Note: the sound effects in sounds/README.txt are still M4A -- that
was a separate choice for those four short clips and doesn't need
to match the music format.)

Volume: both tracks are set to 50% by default in the code, so they
sit under the sound effects rather than fighting them (search for
MUSIC_VOLUME in index.html if you want to adjust that number
yourself -- 0 is silent, 1 is full volume).

IMPORTANT -- same browser rule as sounds/README.txt's note on
credits-appear.m4a: audio can't autoplay until the player has
interacted with the page in some way. walk.mp3 now tries to start as
soon as the credits fade away, which can happen automatically
(no click yet) -- so on a completely cold load, some browsers may
block that first attempt and stay silent. There's a safety net,
though: the moment the player clicks "Start Game," walk.mp3 is asked
to play again, and a real click always satisfies the browser's
requirement -- so at worst, the music is a beat or two late on a
brand-new visit, never permanently silent. choice.mp3 only ever
starts after a plant is tapped, which is always a click, so it's not
affected by this at all.

Until these files exist, the game just plays silently -- nothing
breaks. You can delete this file once both are in place.
