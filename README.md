# A Keyboard Level-3/4 Layout Add-on for Esperanto #

This is a modification of the `/usr/share/X11/xkb/symbols/epo` file.
That file contains several layouts for inputting text in Esperanto.
Only one input method is retained in the modification: the supersigned
letters of Esperanto are located at the Level-3/4 under their respective
base letters of a Latin keyboard (say, “US-basic”), so that

 * `ĉ` = `AltGr`+`ĉ`
 * `Ĉ` = `AltGr`+`C` (i.e. `AltGr`+`Shift`+`c`)

The alternative *direct methods* (`ĉ` replaces `x` at Level‑1, `x` is
typed as `AltGr`+`x`) breaks the software developed for the standard
US layout: `Ctrl`+`x` becomes `Ctrl-ĉ` etc, and the *Common User Access*
System (CUA) becomes unusable. (Direct method is available and quite
convenient in an intelligent editor like Emacs.) At the global OS level
the direct methods are impractical, and they are removed from this `epo`.

The converse method which puts the supersigned Esperanto letters at
the Level‑3/4 was already there in the Ubuntu’s `epo` file; it is less
convenient for typing in Esperanto, but it correctly works with the
standard software designed for use with an ASCII keyboard (in the
converse method the Level‑1/2 layout is left unchanged). Therefore I 
adopt this converse method for the system-wide esperantization; the
direct method, which puts all the esperantic letters al the Level-1/2, I
implement and use in Emacs, which is intelligent enough to spare me
most of the layout switching.

OTOH the project’s `epo` adds some useful characters, required by the
Esperantic tradition: curly apostrophes, paired quotation marks, en-
and em-dashes, non-breakable spaces and hyphens etc. These additions
are done for the QWERTY layout only; the Dvorak and Colemak layouts
remain unchanged.

# The enriched QWERTY layout #

~~~
┌─────┐
│ 2 4 │   2 = Shift,  4 = AltGr + Shift
│ 1 3 │   1 = Normal, 3 = AltGr
└─────┘
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓
│ ~ ˞ │ ! ′ │ @ ə │ # ɜ │ $ £ │ % ˌ │ ^ ↑ │ & † │ * • │ (   │ ) ° │ _ ‑ │ + ~ ┃ ⌫ Back  ┃
│ ` ‘ │ 1 ¹ │ 2 ² │ 3 ³ │ 4 § │ 5 ˈ │ 6 ↓ │ 7 { │ 8 } │ 9 [ │ 0 ] │ - ‒ │ = ≈ ┃  space  ┃
┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫
┃       ┃ Q   │ W   │ E ɛ │ R   │ T   │ Y   │ U Ŭ │ I   │ O   │ P   │ {   │ }   ┃ Enter ┃
┃Tab ↹  ┃ q   │ w   │ e € │ r   │ t   │ y   │ u ŭ │ i   │ o   │ p   │ [ 〈 │ ] 〉 ┃   ⏎   ┃
┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓      ┃
┃        ┃ A ɑ │ S Ŝ │ D   │ F   │ G Ĝ │ H Ĥ │ J Ĵ │ K   │ L   │ : “ │ " ” │ | | ┃      ┃
┃Caps ⇬  ┃ a ª │ s ŝ │ d   │ f   │ g ĝ │ h ĥ │ j ĵ │ k   │ l   │ ; „ │ ' ’ │ \ ¦ ┃      ┃
┣━━━━━━━━┻━━━━┱┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫
┃             ┃ Z ʒ │ X   │ C Ĉ │ V ʌ │ B ″ │ N ⁿ │ M μ │ < „ │ > · │ ? ʔ ┃             ┃
┃Shift ⇧      ┃ z « │ x » │ c ĉ │ v ‹ │ b › │ n – │ m — │ , ‚ │ . … │ / ʼ ┃Shift ⇧      ┃
┣━━━━━━━┳━━━━━┻━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛
┃       ┃  ◆  ⌘ ┃       ┃ ␣ sp                      nnbsp ⍽ ┃       ┃       ┃       ┃
┃Ctrl ⎈ ┃Logo ⊞ ┃Alt  ⎇ ┃ ␣ sp        Space          nbsp ⍽ ┃AltGr ⇮┃Menu   ┃Ctrl ⎈ ┃
┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛
~~~

Disambiguation of similar glyphs:
* `AltGr`+`-` produces “figure dash”, as in ‒2;
* `AltGr`+`n` produces en-dash, as in 0–9;
* `AltGr`+`m` produces em—dash;
* `AltGr`+`5` is “primary ˈstress”
* `AltGr`+`Shift`+`1` produces prime′, as in 45°20′17″;
* `AltGr`+`B` (i.e. `AltGr`+`Shift`+`b`) produces bis″ (= double-prime″);
* `AltGr`+`:` and `AltGr`+`"` produce “US quotation marks”;
* `AltGr`+`,` (`AltGr`+*comma*) produces “single low-9 quotation mark” (U+201A = ‹‚›);
* `AltGr`+`%` is “ˌsecondary stress” (cf [SAMPA](https://en.wikipedia.org/wiki/SAMPA_chart)) or Zamenhof’s *signeto* (as in ‹malˌsanˌulˌo›) 
* `AltGr`+`Shift`+`.` produces *middle dot*, as in ‹mal·san·ul·o›;
* `AltGr`+`/` produces *letter apostrophe* (U+20BC), as in «Ho, mia korʼ»;
* `AltGr`+`[` and `AltGr`+`]` produce *angle brackets* (as in ‘〈a, b〉’);
* `AltGr`+`v` and `AltGr`+`b` produce *half-guillemots* (as in *la artikolo ‹lʼ›*).
* `nbsp` = “Non-Breaking Space” (U+00A0), `nnbsp` = “Narrow NBSP” (U+202F)

## Compose key (⎄) can be handy ##

This modification includes no dead key or accented letter (apart from
those of Esperanto), because there are too many of them and they can
be easily combined with the help of the regular
[Compose key](https://en.wikipedia.org/wiki/Compose_key) ⎄. But some
typographic characters, important for Esperanto (e.g. the lower
99-quotation mark ‹„›) are duplicated in `epo` because their
Compose-combinations are much longer and/or unintuitive.

Thus there is no key for any of the following characters:

* Currency Symbols:
  + ₿ : ‘⎄ `B |`’
  + ¢ : ‘⎄ `c |`’
  + € : ‘⎄ `E =`’   or   ‘⎄ `e =`’   or   ‘⎄ `C =`’   or   ‘⎄ `= C`’ …
  + £ : ‘⎄ `- L`’ 
  + ¥ : ‘⎄ `Y =`’   or   ‘⎄ `= y`’ …
* Ligatures and Diacritics:
  + æ : ‘⎄ `a e`’
  + ß : ‘⎄ `s s`’
  + è : ‘⎄`` ` e``’;   ë : ‘⎄ `" e`’;  ę : ‘⎄ `; e`’;   ç : ‘⎄ `, c`’ …
  + î : ‘⎄ `^ i`’ (but **ĉĝĥĵŝ** are *also* available as special Level-3 keys in this layout)
  * ø : ‘⎄`` / o``’   or   ‘⎄`` o /``’;   Ł : ‘⎄ `/ L`’ …
  * ž : ‘⎄`` z <``’   or   ‘⎄ `v z`’ …
  
## Caveat ##

This extension should work as expected with any QWERTY as long as the
Level‑3/4 definitions of the layouts in question do not collide. I use it
with the `basic` variant of the `us` layout. But if you use the
“French (Canada)” layout, some collisions would emerge. Actually
“French (Canada)” by itself provides some of my additions, and quite a
few of them occupy the same keys — e.g. the quotation marks
Z/‘«’, X/‘»’ etc.[^1]

~~~
┱─────┬─────┬─  ─┬─────┬─────┬─────┬─────┬─────┲┷━━━━━┻━━━━━━┫
┃ Z   │ X   │    │ N   │ M μ │ < „ │ > · │ ? ʔ ┃             ┃
┃ z « │ x » │    │ n – │ m — │ , ‚ │ . … │ / ʼ ┃Shift ⇧      ┃
──────┴─────┴─  ─┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛
~~~

(yet  it  does not  provide  the  *letter  apostrophe* and  the  lower
99-quotation  mark ‹„›);  in that  case  all you  need is  to use  the
original `epo`  from the  distribution, which  adds diacritics  to the
base letters  CGHJSU only, and  “French (Canada)” defines  nothing for
their keys at the Level‑3/4.

(Yet the distro’s `epo` too can collide with another QWERTY layout, if
the latter does use any of the CGHJSU keys at the levels 3 or 4.)

[^1]: The new `epo` additions in some cases follow the Canadian
arrangement, e.g. in location of the quotation marks: Z/‘«’, X/‘»’ etc.

# Installation #

The easiest way to install this `epo` is to replace the standard one.
In Ubuntu its standard location is `/usr/share/X11/xkb/symbols/epo`;
if you use a different Linux distro, please check that its `epo`
file is located there (in other Linux distributions it may reside at
`/etc/X11/xkb/symbols/epo`).
If the new modified `epo` is in the current directory, just say
~~~
sudo cp epo /usr/share/X11/xkb/symbols/
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

sets `ralt` (= `AltGr`) as a Level‑3/4 switch, and adds the `epo`
definitions to the current layout.

You can combine that command with specification of some different
layout(s) and their switches, e.g.

~~~
setxkbmap -layout "us,ru" -variant "basic,phonetic" -option grp:shift_caps_switch,lv3:ralt_switch,esperanto:qwerty,compose:menu
~~~

This defines 2 layouts: US and Russian, respectively in their `basic`
and `phonetic` variants; they are turned on with CapsLock and
CapsLock+Shift respectively; AltGr (while pressed) turns on Level‑3/4;
epo definitions are added to the US basic QWERTY layout; the Menu key
acts as the Compose key.

Such a command could be put e.g. into the `autostart` script file of the OpenBox window manager.

### From GUI ###
GUI paths vary from system to system; here is the Linux Mint way:

> (**LM** Logo) → System Settings → Keyboard → Layouts / (Options)
>> ► Esperanto letters with superscripts
>>> ○ Default\
>>> ○ Colemak\
>>> ○ Dvorak\
>>> • QWERTY

# Sticky Keys #

I’ve got used to the complicated chords of Emacs, but for some reason
the Level4 combinations `AltGr`+`Shift`+… are difficult for me. An
obvious solution is to use `StickyKeys` — either
[via GUI](https://help.ubuntu.com/stable/ubuntu-help/a11y-stickykeys.html.en),
or [from CLI](https://superuser.com/questions/410657/enabling-sticky-keys-under-xorg-awesome-desktop-manager).

Alas, this is an overkill which makes sticky *all* the modifier keys. I
want only AltGr to be sticky, but “this is not user serviceable” in a
regular way. Yet I was able to implement it as the Option 2 of
[this recipe](https://unix.stackexchange.com/questions/591754/make-specific-key-sticky). 
With this approach the above `setxkbmap` command becomes
~~~
setxkbmap -layout "us,ru" -variant "basic,phonetic" -option grp:shift_caps_switch,lv3:ralt_switch,esperanto:qwerty,compose:menu,altgr:latch
~~~
