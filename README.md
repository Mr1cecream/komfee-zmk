# komfee-zmk
This repository contains the firmware for the [komfee keyboard](https://github.com/Mr1cecream/komfee).

## Customizing

### zmk-config (recommended)
Follow the [zmk-config set-up guide](https://zmk.dev/docs/user-setup).  
Then add to your `config/west.yml`:
```yml
projects:
    - name: zmk
    # ...
    - name: komfee-zmk
      remote: mr1cecream
      revision: main
      import: config/west.yml
```
and to your `build.yaml`:
```yaml
include:
  - board: nice_nano_v2
    shield: komfee_left
  - board: nice_nano_v2
    shield: komfee_right
```

You can then create a `config/komfee.keymap` where you may customize the keymap.  
Push the changes to your zmk-config repository and the firmware will be built by GitHub Actions.

### Fork
You may fork this repository and edit the default keymap at [/boards/shields/komfee/komfee.keymap](boards/shields/komfee/komfee.keymap).
