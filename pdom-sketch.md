# Faraday's Law

## Alerts

Movement Alert: Cursor key move in new direction, or step size change
* _"`[step direction]` 1 `[step size]` step."_
* `step direction` values:
    * left
    * right
    * up
    * down
* `step size` values:
    * `regular` (default)
    * `large` (_if CTRL modifier pressed_)
    * `small` (_if Shift modifier pressed_)
* Alert Frequency:
    * on movement direction change
    * when a step is made using a different step size than before.

Movement Alert: Cursor key move in the same direction as before
* _"`[step direction]`"_
* Alert Frequency:
    * This is a lower priority alert. If one of the other alerts / events has occurred it is not be necessary to give this movement alert.

Jump start alert:
* _"Jumping magnet `[jump speed]` to `[jump direction]` side of play area. Press Space to stop jump."_
* `[jump speed]` values:
    * `slowly` (_1 key pressed_)
    * `normally` (_2 key pressed_)
    * `quickly` (_3 key pressed_)
* `[jump direction]` values:
    * `left`
    * `right`
* Alert Frequency:
    * 
* **Remark:** the word "jump" seems appropriate because:
    1. it is a friendly term
    2. approximately describes the motion
    3. conceptually distinct from the other magnet movement term "Moving"

Jump stop alert:
* "Magnet stopped at `[location]` of play area. `[coil proximity]` 4-loop coil. `[coil proximity]` 2-loop coil (_only if 2-loop coil is enabled_)."

Jumping in progress:
* "Jumping to `[left / right]`."
* Alert Frequency: This alert event occurs periodically.

Location change event:
* "At `[location]`  of play area."
* `location` values:
     * `top-left`
     * `top-center`
     * `top-right`
     * `middle-left`
     * `middle-right`
     * `center`
     * `bottom-left`
     * `bottom-center`
     * `bottom-right`
     * +`edge` if at edge
     * +`corner` if at corner
* Alert Frequency: This alert event occurs only  when the magnet transitions from one location region into another.

Coil proximity change event:
* "`[coil proximity]` 4-loop coil."
* "`[coil proximity]` 2-loop coil." (_only if 2-loop coil is enabled_)
* `coil proximity` values:
    * `Far from`
    * `Close to`
    * `Very close to`
    * `In`
* Alert Frequency: This alert event occurs only when the magnet transitions from one proximity region into another.

Coil proximity change event with magnetic field enabled:
* "`[coil proximity]` 4-loop coil and `[field strength]` magnetic field passing through."
* "`[coil proximity]` 2-loop coiland `[field strength]` magnetic field passing through." (_only if 2-loop coil is enabled_)
* `field strength` values:
    * `Very strong`
    * `Strong`
    * `Weak`
    * `Very weak`
    * `Minimal`


**Remarks:**
* Movement, coil proximity and location change alerts may be sufficient to give sense of progress in most cases.
* For blank steps, it may be appropriate to periodically give a location or coil proximity change event, or a movement alert.
* For quick moments, multiple alerts may occur within a small window. It may be necessary to prioritize alerts to report.

Volt meter:
* "`[Connecting / removing]` volt meter to circuit"

Magnetic field add/remove:
* "`[Showing / hiding]` magnetic field lines."

2 loop coil add/remove:
* "`[Adding / removing]` 2 loop coil `[to / from]` circuit."

Flipping magnet:
* "Flipping magnet: North pole is now on `[left / right]`. South pole now on `[right / left]`."

Flipping magnet with field lines visible:
* "Flipping magnet and its magnetic field: North pole is now on `[left / right]`. South pole now on `[right / left]`."

## Scene Summary

* Simulation Play Area contains a circuit and a magnet.

* Currently, the a circuit consists of a lightbulb, `a volt meter`, `2 loop coil`, and a 4 loop coil. These parts are connected together with wires to form the circuit.

* The magnet is at the `[location]` of the Play Area. The magnet has two magnetic poles: North on the `[left / right]`, South on the `[right / left]`.

* Move the magnet to play.

## Play Area

### Circuit

The circuit consists of a lightbulb, `a volt meter`, `2 loop coil`, and a 4 loop coil. All of these parts are connected together with some wires to form the circuit.

**Checkbox**: Add / remove volt meter

**Checkbox**: Add / remove 2 loop coil

**Remark:** _The description of the magnetic field below gets reported as an update (aria live region?). -jh_

   * "`[field strength]` magnetic field is passing through the 4 loop coil."
   * "`[field strength]` `magnetic field` is passing through the 2 loop coil."

**Checkbox**: show / hide magnetic field

### Magnet

The magnet is at the `[location]` of the Play Area. Use the arrow keys to move the magnet. Press H for additional keyboard commands.

The magnet is `[proximity]` to the 4-loop coil (, and is `[proximity]` to the 2-loop coil).

The North pole is on the `[left / right]`, South pole is on the `[right / left]`.

**Remark:** _The description of the magnetic field below gets reported as an update (aria live region?). -jh_

* "The magnetic field is going from North pole on `[left / right]` end, to South pole on `[right / left]` end of magnet."

**Button**: flip magnet
