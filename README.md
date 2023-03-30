# `west`-based Custom ZMK Configuration for MoErgo Glove80

![MoErgo Logo](moergo_logo.png)

This template repository provides `west`-based ZMK configuration for the MoErgo Glove80 wireless split contoured keyboard.
You can use this template repository to develop your own keymap and build your own ZMK firmware to run on your Glove80 using ZMK/Zephyr's upstream `west` toolchain.

**NOTE: You can also customize the layout of your Glove80 keyboard with the [Glove80 Layout Editor](https://my.glove80.com) web app, or the [official ZMK configuration repository template](https://github.com/moergo-sc/glove80-zmk-config).
For most users, the Glove80 Layout Editor is the recommended and simpler option. More information is available at the official MoErgo Glove80 Support site (see resources below).**

These steps will get you using your keymap on your keyboard in the fastest time possible. It uses the GitHub Actions feature to build your firmware online.

If you are looking to dig deeper into ZMK and develop new functionality, it is recommended to follow the steps of installing ZMK as found on the official ZMK documentation site (linked below).

## Resources
- The [official MoErgo Glove80 Support](https://moergo.com/glove80-support) web site. Glove80 documentation and other technical resources.
- The [official MoErgo Discord Server](https://moergo.com/discord). Instant conversations with other Glove80 users.

- The [official ZMK Documentation](https://zmk.dev/docs) web site. Find the answers to many of your questions about ZMK Firmware.
- The [official ZMK Discord Server](https://discord.gg/8cfMkQksSB). Instant conversations with other ZMK developers and users. Great technical resource!

- The [official Glove80 ZMK Distribution](https://github.com/moergo-sc/zmk). Repositiory for ZMK firmware customized for Glove80.

## Instructions
1. Log into, or sign up for, your personal GitHub account.
2. Create your own repository using this repository as a template ([instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template])) and check it out on your local computer.
3. Add your chosen configuration such as keymap to the `config` directory as described in [the ZMK documentation](https://zmk.dev/docs/user-setup)
4. Commit and push your changes to your personal repo. Upon pushing it, GitHub Actions will start building a new version of your firmware with the updated keymap.

## Firmware Files
To locate your firmware files and reflash your Glove80:
1. log into GitHub and navigate to your personal config repository you just uploaded your keymap changes to.
2. Click "Actions" in the main navigation, and in the left navigation click the "Build" link.
3. Select the desired workflow run in the centre area of the page (based on date and time of the build you wish to use). You can also start a new build from this page by clicking the "Run workflow" button.
4. After clicking the desired workflow run, you should be presented with a section at the bottom of the page called "Artifacts". This section contains the results of your build, in a file called `firmware.zip`.
5. Download `firmware.zip` and extract it to reveal two files, `glove80_lh-zmk.uf2` and `glove80_rh-zmk.uf2`: these are the firmware for the left and right sides of the keyboard respectively.
6. Flash the firmware to Glove80 according to the user documentation on the official Glove80 Support website (linked above). *Note that unlike firmware built with the standard Glove80 toolchain, you must select the correct firmware file to upload to each half of the keyboard.*

Your keyboard is now ready to use.
