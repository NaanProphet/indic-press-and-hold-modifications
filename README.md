# indic-press-and-hold-modifications
Modifying Mac OS X's default keyboard Press and Hold accents to include commonly romanized characters used in Indian languages (e.g. ṇ, ṣ, etc.)

Successfully tested on 10.13.3 High Sierra on a MacBook Air 6,2.

## Install Prep (OS X 10.11 El Capitan onwards)

Disable System Integrity Protection first, in order to edit these files:

1. Boot into the Recovery HD by restarting whilst holding ⌘R

2. Open Terminal (from the Utilities menu)

3. Run the following command in Terminal:

   ```
   csrutil disable
   ```

4. Restart

## Install

Replace the respective plist file inside (creating a backup first). It can be helpful to double check the differences first using the `diff` command.
* For OS X 10.12 Sierra onwards
```
/System/Library/Input Methods/PressAndHold.app/Contents/PlugIns/PAH_Extension.appex/Contents/Resources
```
***No restart is required.*** Optionally boot into Recovery mode and enable System Integration Protection again with the `csrutil enable` command.

## Additional characters added
* Ḍ D̥ (new group)
* Ḥ (new group)
* Ṇ Ṅ
* Ṛ (new group)
* Ṣ
* Ṭ (new group)
* ḍ d̥ (new group)
* ḥ (new group)
* ṁ mँ (new group)
* ṇ ṅ
* ṛ (new group)
* ṣ
* ṭ (new group)

Note: for all new groups, i arbitrarily chose `<Direction>left</Direction>` but am not sure if it matters.

## References
* http://apple.stackexchange.com/questions/49565/how-can-i-expand-the-number-of-special-characters-i-can-type-using-my-keyboard
* http://apple.stackexchange.com/questions/208911/the-keyboards-plists-of-pressandhold-also-can-no-longer-be-modified-to-add-the
