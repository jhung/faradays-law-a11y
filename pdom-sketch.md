# Faraday's Law

## Alerts

Cursor key move in new direction:
* "Moving magnet 1 step `[left / right / up / down]`."

Cursor key move in the same direction as before:
* 1st and 2nd step:
    * "Moving magnet 1 step."
* 3rd step:
    * "Moving magnet 1 step. At `[location]` of play area."
* `location` values:
     * `top-left` / `top-center` / `top-right`
     * `middle-left` / `middle-right`
     * `center`
     * `bottom-left` / `bottom-center` / `bottom-right`
* **Remark 1:** the intention is to periodically give a slightly more detailed description to give sense of progress and orient the player.
* **Remark 2:** BASE does something like this and Faraday should follow a similar strategy.

Movement keys + CTRL:
* "Moving magnet 1 large step..."

Movement keys + Shift:
* "Moving magnet 1 small step..."

Movement with region transition:
* "`[Movement alert text from above]`. At `[location]` of play area."
* `location` values:
     * `top-left` / `top-center` / `top-right`
     * `middle-left` / `middle-right`
     * `center`
     * `bottom-left` / `bottom-center` / `bottom-right`

Initiating jumping magnet:
* "Jumping magnet quickly to `[left / right]` side of play area."
* "Jumping magnet slowly to `[left / right]` side of play area."
* "Jumping magnet to `[left / right]` side of play area."

Region transition while jumping in progress:
* "Jumping to `[left / right]`. At `[location]` of play area."
* `location` values:
     * `top-left` / `top-center` / `top-right`
     * `middle-left` / `middle-right`
     * `center`
     * `bottom-left` / `bottom-center` / `bottom-right`
* **Remark:** It may be necessary to provide additional text alerts for slow jumping and in edge areas where sonification may not occur. User testing may reveal what approach to take.

## Polite Alerts

Volt meter:
* `Connecting / removing] volt meter to circuit`
* `Removing volt meter to circuit`

Magnetic field add/remove:
* `Showing magnetic field lines.`
* `Hiding magnetic field lines.`

2 loop coil add/remove:
* `Adding 2 loop coil to circuit.`
* `Removing 2 loop coil from circuit.`

Flipping magnet:
* `Flipping magnet: South pole is now on left. North pole now on right.`
* `Flipping magnet: North pole is now on left. South pole is now on right.`

Flipping magnet with field lines visible:
* `Flipping magnet and its magnetic field: South pole is now on left. North pole now on right.`
* `Flipping magnet and its magnetic field: North pole is now on left. South pole is now on right.`

## Scene Summary

* Simulation Play Area contains a circuit and a magnet.

* Currently, the a circuit consists of a lightbulb, `a volt meter`, `2 loop coil`, and a 4 loop coil. These parts are connected together with wires to form the circuit.

* The magnet is at the `middle-right side` of the Play Area. The magnet has two magnetic poles: North on the `left`, South on the `right`.

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

The magnet is at the `middle-right side` of the Play Area.
The North pole is on the `left`, South pole is on the `right`.

**Remark:** _The description of the magnetic field below gets reported as an update (aria live region?). -jh_

* `The magnetic field lines are going from North pole on left end, to South pole on right end of magnet.`

**Button**: flip magnet
