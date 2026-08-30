Sound effects — six files

Drop files into this folder (sounds/, same level as images/) with
these exact names. Nothing else needs to change in the code -- each
one plays automatically as soon as it's here.

  credits-appear.m4a   Plays right as the credits screen appears and
                        its logo starts fading in -- the very first
                        thing in the whole game. See the important
                        note about this one below.

  hunger-low.m4a        Plays once right as the hunger meter crosses
                        into the danger zone (1/4 full, the same
                        moment the meter starts flashing red) -- not
                        on every frame it stays low, just that one
                        crossing. Free to play again later in the
                        same run if hunger dips that low a second
                        time (a correct pick refills it above the
                        threshold in between).

  correct.m4a           Plays the instant the player picks the
                        FRIEND card (the edible one) in an encounter.

  wrong.m4a              Plays the instant the player picks the FOE
                        card (the poisonous one) in an encounter.

  game-over.mp3          Plays the instant the Game Over screen
                        appears (running out of hearts) -- not the
                        Win screen, just the loss state. A short
                        sting works well here; it doesn't need to
                        loop. MP3, not M4A like the others above --
                        that was a deliberate, separate choice.

  rescue.mp3             Plays the instant the Win/Rescue screen
                        appears (reaching the helicopter). Also MP3,
                        also a short sting, also doesn't need to loop.

Format: game-over.mp3 and rescue.mp3 are MP3. Everything else above
is M4A (AAC) -- all current major browsers (Chrome, Firefox, Safari,
Edge) play both formats natively through the same audio code this
game already uses, so whichever format you've already got a given
sound in -- straight out of GarageBand, Voice Memos, a phone
recording, whatever -- there's usually no need to convert it, just
drop the file in as-is with the right extension from the list above.

If you ever do need to convert something (say you only have an MP3
but need an M4A, or vice versa), the free, no-install-needed option
is an online converter -- search "convert to m4a" (or "convert to
mp3") and any of the common ones (e.g. cloudconvert.com) will do it
in a browser. If you'd rather have a proper desktop tool: ffmpeg
(free, command-line -- ffmpeg -i input.mp3 -c:a aac -b:a 192k
output.m4a, or drop the -c:a aac part and name the output .mp3 to go
the other way) or Audacity (free, has a simple Export menu) both
handle it well. None of this is needed unless you end up with a file
in the wrong format first.

Keep them short and punchy -- these are one-shot sound effects, not
music. A few hundred milliseconds to a couple of seconds is normal
for correct/wrong/hunger-low/game-over/rescue. credits-appear.m4a can
run a little longer if it's meant to underscore the whole logo card,
but even that only needs to cover roughly its 2.2-second fade in/
hold/fade out (see index.html's CREDITS_FADE_MS/CREDITS_HOLD_MS
comments if you want the exact numbers) -- anything after that plays
under a black screen nobody's looking at.

IMPORTANT -- about credits-appear.m4a specifically: browsers block
audio from playing automatically until the player has interacted
with the page in some way (a click, a tap, a keypress) -- and the
credits screen is the very first thing shown, before any of that has
happened. So on a completely cold load, this one sound may stay
silent in some browsers (Chrome in particular), while the other five
will always play fine since by then the player has already clicked
Start, tapped a card, lost a heart, or won. This is a browser policy,
not a bug in the game -- there isn't a reliable way around it for a
sound meant to play with zero prior interaction. If it turns out to
matter a lot for the jam, one option later is having the credits
screen itself require a "tap to begin" first (that tap would count as
the interaction) -- but that changes the intro from fully automatic
to a one-tap start, so it's your call whether that trade-off's worth
it.

Until these files exist, playing a sound just fails silently --
nothing breaks, nothing errors, the game plays exactly the same
minus the sound. You can delete this file once all six are in place.
