# Layer3 Layout Add-on for Esperanto #

This is a modification of the `/usr/share/X11/xkb/symbols/epo` file.
That file contains several layouts for inputting text in Esperanto.
Only one input method is retained in the modification: the supersigned
letters of Esperanto are located at the Level3 under their respective
base letters of a Latin keyboard (say, “US-basic”), so that

 * `ĉ` = `AltGr`+`ĉ`
 * `Ĉ` = `AltGr`+`C` (i.e. `AltGr`+`Shift`+`c`)

The alternative *direct methods* (`ĉ` replaces `x` at Level1, `x` is
typed as `AltGr`+`x`) breaks the software developed for the standard
US layout: `Ctrl-x` becomes `Ctrl-ĉ` etc, and the *Common User Access*
System (CUA) becomes unusable. (Direct method is available and quite
convenient in an intelligent editor like Emacs.) At the global OS level
the direct methods are unpractical, and they are removed from this `epo`.

The “Diacriticals at Level3” method was already there in the Ubuntu’s
`epo` file; this project’s `epo` adds more useful characters, required
by the Esperantic tradition: curly apostrophes, paired quotation
marks, en- and em-dashes, non-breakable spaces and hyphens etc. These
additions are done for the QWERTY layout only; the Dvorak and Colemak
layouts remain unchanged.

# The enriched QWERTY layout #

~~~
┌─────┐
│ 2 4 │   2 = Shift,  4 = Level3 + Shift
│ 1 3 │   1 = Normal, 3 = Level3
└─────┘
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓
│ ~ ‘ │ !   │ @ ″ │ # № │ $ £ │ %   │ ^ ↑ │ & ‡ │ * ∞ │ (   │ )   │ _ ‑ │ + × ┃ ⌫ Back  ┃
│ ` ʼ │ 1 ¹ │ 2 ² │ 3 ³ │ 4 § │ 5 ÷ │ 6 ↓ │ 7 † │ 8 • │ 9   │ 0 ° │ - ‒ │ = ≈ ┃  space  ┃
┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫
┃       ┃ Q   │ W   │ E   │ R   │ T   │ Y   │ U   │ I   │ O   │ P   │   { │   } ┃ Enter ┃
┃Tab ↹  ┃ q   │ w   │ e € │ r   │ t   │ y   │ u   │ i   │ o   │ p   │   [ │   ] ┃   ⏎   ┃
┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓      ┃
┃        ┃ A   │ S Ŝ │ D   │ F   │ G Ĝ │ H Ĥ │ J Ĵ │ K   │ L   │ : “ │ " ” │ |   ┃      ┃
┃Caps ⇬  ┃ a ª │ s ŝ │ d   │ f   │ g ĝ │ h ĥ │ j ĵ │ k   │ l   │ ; „ │ ' ’ │ \ ¦ ┃      ┃
┣━━━━━━━━┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫
┃             │ Z ‹ │ X › │ C Ĉ │ V ‘ │ B ’ │ N ⁿ │ M μ │ < „ │ > · │ ?   ┃             ┃
┃Shift ⇧      │ z « │ x » │ c ĉ │ v “ │ b ” │ n – │ m — │ , ‚ │ . … │ / ⁄ ┃Shift ⇧      ┃
┣━━━━━━━┳━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛
┃       ┃       ┃       ┃ ␣ sp                      nnbsp ⍽ ┃       ┃       ┃       ┃
┃Ctrl   ┃Meta   ┃Alt    ┃ ␣ sp        Space          nbsp ⍽ ┃AltGr ⇮┃Menu   ┃Ctrl   ┃
┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛
~~~

It should be noted that
* `AltGr`+`\`` (`AltGr`+*grave*) produces *letter apostrophe* (U+20BC);
* `AltGr`+`,` (`AltGr`+*comma*) produces “single low-9 quotation mark” (U+201A, ‹‚›);
* `AltGr`+`-` produces “figure dash”; 
* `AltGr`+`n` produces en-dash; 
* `AltGr`+`m` produces em-dash. 

## Some Limitations ##

This extension should work as expected with any QWERTY as long as the
Level3 definitions do not collide. I use it with the `basic` variant
of the `us` layout. But if you use the “French (Canada)” layout, some
collisions would emerge. Actually “French (Canada)” by itself provides
most of these additions[^1] (yet it does not provide the *letter
apostrophe* and the lower 99-quotation mark ‹„›); in that case all you
need is to use the original `epo` from the distribution, which adds
diacritics to the base letters CGJHSU only, and “French (Canada)”
defines nothing for their keys at the Level3.

[^1]: And the new `epo` additions in some cases follow the Canadian
arrangement, e.g. in location of the quotation marks: Z/‘«’, X/‘»’ etc.

# Installation #

The easiest way to install this `epo` is to replace the standard one.
In Ubuntu its standard location is `/usr/share/X11/xkb/symbols/epo`;
if the new modified `epo` is in the current directory, just say
~~~
sudo epo /usr/share/X11/xkb/symbols/
~~~
More civilized ways to customize keyboard layouts are described in
[Ubuntu documentation](https://help.ubuntu.com/community/Custom%20keyboard%20layout%20definitions).

## Activation ##

The `epo` component can be activated from CLI or GUI. 

### From CLI ###
The command

~~~
setxkbmap -option lv3:ralt_switch,esperanto:qwerty
~~~

sets `ralt` (= `AltGr`) as a Level3 switch, and adds the `epo`
definitions to the current layout.

You can combine that command with specification of some different
layout(s) and their switches, e.g.

~~~
setxkbmap -layout "us,ru" -variant "basic,phonetic" -option grp:shift_caps_switch,lv3:ralt_switch,esperanto:qwerty,compose:menu
~~~

This defines 2 layouts: US and Russian, respectively in their `basic`
and `phonetic` variants; they are turned on with CapsLock and
CapsLock+Shift respectively; AltGr (while pressed) turns on Level3;
epo definitions are added to the US basic QWERTY layout; the Menu key
acts as the Compose key.

Such a command could be put e.g. into the `autostart` script file of the OpenBox window manager.

### From GUI ###
GUI paths vary from system to system; here is the Linux Mint way:

> (**LM**) → System Settings → Keyboard → Layouts / (Options)
>>> ► Esperanto letters with superscripts
>>>>>>> ○ Default
>>>>>>> ○ Colemak
>>>>>>> ○ Dvorak
>>>>>>> • QWERTY


