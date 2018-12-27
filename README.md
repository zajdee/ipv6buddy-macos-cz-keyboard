# ipv6buddy-macos-cz-keyboard
This repository adds support for the [IPv6 Buddy](https://www.ipv6buddy.com/) keyboard (**Euro version**) on MacOS with Czech keyboard layout.

All you need is to:

1. install [Karabiner Elements](https://pqrs.org/osx/karabiner/index.html) (don't forget to enable kernel extension as suggested by the app)
2. `cp karabiner-elements-ipv6buddy-cz.json ~/.config/karabiner/assets/complex_modifications/`
3. open `Karabiner`
4. click `Complex Modifications`
5. click `Rules`
6. click `Add rule`
7. In the `IPv6 Buddy (CZ)` section, click on the `Enable` button next to `Use IPv6 Buddy with Czech keyboard`

And that's it! **Enjoy your IPv6 Buddy.**

What works and what doesn't:

- numeric keys (`0..9`)
- alpha keys (`a..f`)
- dot key (NOTE: see limitations section below for the case when Shift is pressed)
- colon and double-colon keys
- slash key
- backspace, tab and enter keys

Known limitations:

- if you press the Shift key on your regular keyboard, then press the `Dot` key on IPv6 Buddy, you will get colon instead (the reason is that the colon key on IPv6 buddy actually sends left shift, then dot; while shift is already pressed, it is hard to distinguish if it came from your regular keyboard or from the buddy); this is a minor thing and the `json`-based rules of Karabiner are such a mess - I'm happy to accept a pull request for this, but don't want to spend any more time on getting this to work myself
- if you enable `Caps Lock` mode or press the `Shift` key on your regular keyboard, the `A..F` characters will be in uppercase (that is usually expected, it's mentioned here just for clarity)
- the `US` model of the Buddy is not supported by this repository; only the `Euro` version was tested