### ***buglib v0.2***

Work-in-progress configuration library for TF2. This library is non-intrusive, unlike current alternatives that override configuration files. Load only the modules you want to use.

**Documentation of values and configuration presets is WIP.**

---

### Installation

Add `buglib.vpk` into your `tf/custom` folder. In your `cfg/autoexec.cfg` (create one if needed), add this line:

```java
exec buglib
```

You should see a splash text output into your TF2 console if buglib loaded.

---

### Modules

You can now load modules you want to use, which will also output that they've been loaded in your TF2 console. Modules ***never*** set values for you. They only added commands to make configuring your game easier.

Example using the `null_movement`  module:

```java
exec buglib

// load modules with `load@module_name`
load@null_movement

// cycle crosshair colors
cycle_crosshair=true

// cardinal
bind w +null_forward
bind a +null_moveleft
bind s +null_back
bind d +null_moveright

// vertical
bind shift +null_duck
bind space +null_duckjump
```

You can also use `load@all` to load all modules.

---

### Configs

Modules may also come with configs that set values for you. Example from the `gfx` module:

```java
exec buglib

// configs are ran with `module:config_name`
load@gfx
gfx:toaster

// we can still set values ourself, of course
props=1
texture_filter=1
```