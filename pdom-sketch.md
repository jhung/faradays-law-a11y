# Faraday's Law

## Alerts

Movement Alert: Cursor key move in new direction
* "Moving `[left / right / up / down]` 1 step."
* "Moving `[left / right / up / down]` 1 large step." (_if CTRL modifier pressed_)
* "Moving `[left / right / up / down]` 1 small step." (_if Shift modifier pressed_)

Movement Alert: Cursor key move in the same direction as before
* "Moving 1 step."
* "Moving 1 large step." (_if CTRL modifier pressed_)
* "Moving 1 small step." (_if Shift modifier pressed_)
* **Remark:** This is a lower priority alert. If one of the other alerts / events occur it may not be necessary to give this movement alert.

Jump start alert:
* "Jumping magnet slowly to `[left / right]` side of play area. Press Space to stop." (_1 key pressed_)
* "Jumping magnet to `[left / right]` side of play area. Press Space to stop." (_2 key pressed_)
* "Jumping magnet quickly to `[left / right]` side of play area. Press Space to stop." (_3 key pressed_)

Jump stop alert:
* "Magnet stopped at `[location]` of play area. `[coil proximity]` 4-loop coil. `[coil proximity]` 2-loop coil (_only if 2-loop coil is enabled_)."

Jumping in progress:
* "Jumping to `[left / right]`."

Location change event:
* "At `[location]` of play area."
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

Coil proximity change event:
* "`[coil proximity]` 4-loop coil."
* "`[coil proximity]` 2-loop coil." (_only if 2-loop coil is enabled_)
* `coil proximity` values:
    * `Far away from`
    * `Close to`
    * `Very close to`
    * `In`

**Remarks:**
* Movement, coil proximity and location change alerts may be sufficient to give sense of progress in most cases.
* For blank steps, it may be appropriate to periodically give a location or coil proximity change event, or a movement alert.
* For quick moments, multiple alerts may occur within a small window. It may be necessary to prioritize alerts to report.

## Polite Alerts

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

* **Remark 1:** _Coil-then-field description: logical structure, but phrasing is awkward. -jh_
   * `4 loop coil` has `strong magnetic field` is passing through.
   * `2 loop coil` has `weak magnetic field` is passing through.
* **Remark 2:** _Field-then-coil description: structuring less logical, but phrasing is more pleasant. -jh_
   * `Strong` `magnetic field` is passing through the `4 loop coil`.
   * `Weak` `magnetic field` is passing through the `2 loop coil`.

**Checkbox**: show / hide magnetic field

### Magnet

The magnet is at the `[location]` of the Play Area.
The North pole is on the `[left / right]`, South pole is on the `[right / left]`.

Use the arrow keys to move the magnet. Also use CTRL or Shift keys with arrow keys to move magnet in large or small steps.

Use number keys 1, 2, or 3 jump magnet to other side of the play area.

**Remark:** _The description of the magnetic field below gets reported as an update (aria live region?). -jh_

* "The magnetic field lines are going from North pole on `[left / right]` end, to South pole on `[right / left]` end of magnet."

**Button**: flip magnet
