Immunity Clock
v1.5
By Quel (qwarlock@gmail.com)

ABSTRACT
a PVP-only addon, Immunity Clock detects when your PVP target or local enemeis become 
immune to fear/seduce/charm type spells. It displays a timer under the target frame 
indicating approximately how much longer the target will be immune, then followed by a 
cooldown timer showing how long before the target can probably become immune again. A 
second pop-up window provides immunity/cooldown tracking for up to 5 targets, allowing 
you to manage multiple targets in a large pvp fight.

USAGE
/ic - shows Immunity Clock help message
/ic on - enables Immunity Clock tracking
/ic off - disables Immunity Clock tracking

Casting Fear (and similar crowd-control spells) when the target is temporarily immune to
such effects wastes mana (especially since fear is continually nerfed) and prevents you
from using more effective tactics. Immunity Clock will detect and alert you when up to
5 targets cast some form of immunity. Depending on which messages you catch, Immunity
Clock's accuracy will vary. If it manages to catch the casting of a buff (say, Will of
the Forsaken) then the immunity timer and subsequent cooldown timer will be quite accurate.
The display window will show the type of immunity used. For example, if an undead player uses
Will of the Forsaken, the display will be: "Billybob (undead)."

If, on the other hand, you miss the buff message and only catch the "is immune" event, then
Immunity Clock guesses based on the target race, class, and level. In this situation, the type
of immunity will be suffixed with a "?" in the display window, like: "Billybob (mage?)." That
indicates that we don't know exactly what kind of immunity Billybob used, but the *most likely*
choice was a mage-specific spell, ice block.

Timers appear under the target frame as well as in a separate window, giving two views of
active clocks. This not only provides additional alerting that the target is immune (in
case you missed the standard game warnings) but also gives you an idea how much longer they
will likely stay immune. You can switch tactics during the immunity period, then revert to
using fear when the cooldown begins.

LIMITATIONS
1. Immunity Clock only tracks players, not NPCs, primarily due to the limitations of
the TargetByName() function causing erratic behavior when many NPCs in the area have
the same name.

2. Immunity Clock provides only an approximate timer. An undead player may have cast
Will of the Forsaken before 5 second before attacking you, but you don't detect the
immunity until you attempt to cast fear.

3. A given player may have more than one method of becoming immune. Immunity Clock
makes its best guess at which method a player has used, but I expect the logic around
this to become more robust as testing continues.

TO DO:
1. Make names in the popup window click-to-target

2. Possibly add additional color coding to the displays to indicate margin of error
between when the target became immune and when you detected it.

3. Improve logic to detect types of immunity used when a given target has more than
one choice.