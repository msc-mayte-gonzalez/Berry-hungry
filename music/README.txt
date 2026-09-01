Background music — one file

Drop a file into this folder (music/, same level as images/ and
sounds/) with this exact name. Nothing else needs to change in the
code -- it plays automatically, looping, as soon as it's here.

  walk.mp3     Plays throughout the whole play screen, from the
               moment the Berry Hungry start screen appears (right as
               the credits fade away, whether that happens on its own
               or by clicking to skip) straight through walking,
               opening plants, reading about them, and picking --
               with no swap or interruption at any point. Starts
               again on "Try Again."

Loop it automatically for as long as the play screen is showing, so
pick something meant to repeat seamlessly (a few bars to maybe a
minute is normal -- it'll just loop back to the start). Pausing the
game (the Pause button) pauses it, and Resume picks it back up --
Start Over / Game Over / Win stop it, since none of those screens
have their own track.

There used to be a second track (choice.mp3) that swapped in while a
plant's card screen was open -- playtest feedback was that the swap
itself read as an interruption, so that's gone now. The three
encounter sound EFFECTS (card-flip/correct/wrong -- see
sounds/README.txt) layer on top of walk.mp3 instead.

Format: MP3 -- every current major browser plays it natively, no
conversion needed if that's already the format you have it in.
(Note: the sound effects in sounds/README.txt are a mix of M4A and
MP3 -- that's a separate choice for those short clips and doesn't
need to match the music format.)

Volume: set low by default in the code, so it sits well under the
sound effects rather than fighting them (search for MUSIC_VOLUME in
index.html if you want to adjust that number yourself -- 0 is
silent, 1 is full volume).

IMPORTANT -- same browser rule as sounds/README.txt's note on
credits-appear.m4a: audio can't autoplay until the player has
interacted with the page in some way. walk.mp3 now tries to start as
soon as the credits fade away, which can happen automatically
(no click yet) -- so on a completely cold load, some browsers may
block that first attempt and stay silent. There's a safety net,
though: the moment the player clicks "Start Game," walk.mp3 is asked
to play again (and again anytime an encounter modal closes), and a
real click always satisfies the browser's requirement -- so at worst,
the music is a beat or two late on a brand-new visit, never
permanently silent.

Until this file exists, the game just plays silently -- nothing
breaks. You can delete this file once it's in place.
