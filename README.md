# DEB

next gen worldedit inspired modern building tools

todo: better name

## Plans

### Commands

- `//op`
  - `//op cancel`
    cancel an operation
  - `//op list`
    list currently running operations
    
    chat message has clickable commands to cancel the operation and teleport to player or the operation's location (if any)
    
    hover event for detailed info (type: fill region: box, coords, player, etc)
  - `//op show`


    show the progress of an operation
    in either bossbar or actionbar,
    flags to show it globally (all players) or a group
    todo
  - `//op pause`
    pause any running operations
  - `//op confirm`
    confirm the operation if there was any collisions detected with other ops
  - `//op history`
    show a history of all operations, one or many players, cancelled or successful ops included.
    
    click events for tp, undo, redo, etc
    
    hover events for detailed info, time etc also included

    
### Regions

should work similar to worldedit with some additions, inspired from photo editing software xd:

- inverting selection
- spherical selection with angles?- select with a filter

### Patterns

Inspired from worldedit, patterns are kinda similar.

Patterns can be:

- A single block
- Multiple blocks
  - noisy randomized (like worldedit)
  - patches
  - checkerboard pattern

    To implement this, we'll probably have a pattern editor of some sorts that can toggle certain flags:
   - repeat (xyz)
   - size
   - scaling

  - gradient (hermitcraft style xd)

Multi-block patterns should have quick access to reroll

### Ignore-Areas

Ignore areas are regions you can save to a collection that ignores any operation's block placement.

This could be useful where you want to do certain operations without completely obliterating your already established build.

### Operations

Most operations should support some "shortcuts" like:

- Scrolling while creating a sphere should modify its size
- Right clicking a corner of a cuboid should implement resizing

deb should support most of worldedit operations

deb should show the user's selection/actions etc using glowing invis entities (like falling sand) or particles or something similar

if enabled, should also let other players see each other's selections/actions

operations should be asynchronous with a configurable task queue

operations should also notify their progress so we can show it to the user

operations should also check for any collisions with other operations and ask the user if they want to proceed

### Commits

optionally code a commit system where the user can stack and preview operations before they commit them

not the direction of this project but a feature where you could "propose changes" to a build could be cool - it could be used in creative servers maybe?

### Objects

Objects are a new concept that allow for better prototyping and faster build manipulation.

For example, in object mode, creating a sphere would save it as an object instead of pasting the blocks.
This would allow you to, for example, change the pattern of it without creating a new sphere.

Objects should also store their patterns like a reference so multiple objects' patterns can be edited.

### Preferences

With this many features and stuff we should add some sort of preferences for users.

- add differient storages
- a "none" storage, preferences would be disabled entirely and the defaults from the config file would be used

### BlockDB integration

If blockdb becomes a thing, we could implement an integration where you can pick builds ingame and also paste them easily (of course you would preview it before you paste)
