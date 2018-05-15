# Faraday's Law

## Alerts

**Movement Alert**
* _"`[step direction]`"_
* Alert Frequency:
    * This is a lower priority alert. If one of the other alerts / events has occurred it is not be necessary to give this movement alert.

**Movement Alert: direction or step size change**
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



**Jump start alert: on release of 1, 2, or 3 key press**
* _"Jumping magnet `[jump speed]` to `[jump direction]` side of play area. Press Space to stop jump."_
* `[jump speed]` values:
    * `slowly` (_1 key pressed_)
    * `normally` (_2 key pressed_)
    * `quickly` (_3 key pressed_)
* `[jump direction]` values:
    * `left`
    * `right`
* **Remark:** the word "jump":
    1. is a friendly term
    2. approximately describes the motion
    3. conceptually distinct from the other magnet movement term "Moving"

**Jump stop alert: Space bar is pressed, bumped into a coil or reached edge of play area**
* _"Jumping stopped."_

**Jumping in progress:**
* _"Jumping to `[left / right]`."_
* Alert Frequency:
    * This is a lower priority alert. If one of the other alerts / events has occurred it is not be necessary to give this movement alert.

**Coil bump alert**
* _"Bumped into [coil type] coil."_
* `coil type` values:
    * 2 loop
    * 4 loop

**Location change event: magnet transitions from one location region into another**
* _"At `[location]`  of play area."_
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

**Coil proximity change event: magnet transitions from one coil proximity region into another**
* _"`[coil proximity]` 4-loop coil. `[coil proximity]` 2-loop coil."_ (_only if 2-loop coil is enabled_)
* `coil proximity` values:
    * `Far from`
    * `Close to`
    * `Very close to`
    * `In`

**Coil proximity change event with magnetic field enabled**
* "`[coil proximity]` 4-loop coil and `[field strength]` magnetic field passing through. `[coil proximity]` 2-loop coil and `[field strength]` magnetic field passing through." (_only if 2-loop coil is enabled_)
* `field strength` values:
    * `Very strong`
    * `Strong`
    * `Weak`
    * `Very weak`
    * `Minimal`

**Volt meter: adding / removing**
* "`[Connecting / removing]` volt meter to circuit"

**Magnetic field: show / hide**
* "`[Showing / hiding]` magnetic field lines."

**2 loop coil: show / hide**
* "`[Adding / removing]` 2 loop coil `[to / from]` circuit."

**Rotate magnet**
* _"Flipping magnet: North pole is now on `[left / right]`. South pole now on `[right / left]`."_

**Rotate magnet: with visible field lines**
* _"Flipping magnet and its magnetic field: North pole is now on `[left / right]`. South pole now on `[right / left]`."_
* Remark: This is the same description as a regular "Rotate Magnet" alert text with the addition of "and its magnetic field".

## Scene Summary

* Simulation Play Area contains a circuit and a magnet.

* Currently, the a circuit consists of a lightbulb, `a volt meter`, `2 loop coil`, and a 4 loop coil. These parts are connected together with wires to form the circuit.

* The magnet is at the `[location]` of the Play Area, `[proximity]` to the 4 loop coil, and `[proximity]` to the 2 loop coil.

* `[field strength]` magnetic field is passing through the 4 loop coil.

* `[field strength]` magnetic field is passing through the 2 loop coil. _(if field lines visible)_

* Move the magnet to play.

## Play Area

### Circuit

The circuit consists of a lightbulb, `a volt meter`, `2 loop coil`, and a 4 loop coil. All of these parts are connected together with some wires to form the circuit.

**Checkbox**: Connect volt meter to circuit

**Checkbox**: Add 2 loop coil to circuit

`[field strength]` magnetic field is passing through the 4 loop coil. `[field strength]` magnetic field is passing through the 2 loop coil. _(if field lines visible)_

**Checkbox**: Show magnetic field

### Magnet

The magnet is at the `[location]` of the Play Area. Use the W A S D keys to move the magnet. Press H for additional keyboard commands.

The magnet is `[proximity]` to the 4-loop coil (, and is `[proximity]` to the 2-loop coil).

The magnet has two magnetic poles: North on the `[left / right]`, South on the `[right / left]`.

"The magnetic field is going from North pole on `[left / right]` end, to South pole on `[right / left]` end of magnet." _(if field lines visible)_

**Button**: flip magnetic polesv
