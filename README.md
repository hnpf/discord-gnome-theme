# Discourse

A GNOME theme for Discord, following the Adwaita style & GNOME Human Interface Guidelines (with whatever the Discord CSS allows).

<picture>
	<source srcset="assets/preview/theme-dark.png" media="(prefers-color-scheme: dark)">
	<source srcset="assets/preview/theme-light.png" media="(prefers-color-scheme: light)">
	<img align="center" src="assets/preview/theme-light.png" alt="Theme preview">
</picture>

## Requirements

1. Vesktop

   Recommended for enabling the Discord's custom titlebar. Enable with Settings > Vesktop Settings > "Discord Titlebar".

   You can still use something else like BetterDiscord - the theme will work but without the usual GNOME headerbar and with BetterDiscord content unthemed.

2. Settings > Language > Choose "English (US)"

   This allows for custom icons due to how they are identified in Discord. You may [localize][css-icons] the theme, but read the localization note.

3. Settings > Plugins > Enable "ThemeAttributes"

   This allows for icons in the server settings modal. Optional, does not affect user settings.

## Installation

Copy the following into the text box located in Settings > Themes > Online Themes:

```
https://raw.githubusercontent.com/hnpf/discord-gnome-theme/master/Discourse.theme.css
```

For local installation, put [Discourse.theme.css][css-main] in `~/.config/vesktop/themes`. It will **auto-update**. the compiled CSS is fetched live from GitHub on each load.

## Configuration

### [Emoji Replace][emoji-replace] allows you to replace discord's with emojis from a different provider (eg. apple, google, facebook...)
1. Simply edit Discourse.theme.css
2. Follow instructions for changing default emoji provider.
3. That's it! 

### Nitro themes

<picture>
	<source srcset="assets/preview/nitro-theme-dark.png" media="(prefers-color-scheme: dark)">
	<source srcset="assets/preview/nitro-theme-light.png" media="(prefers-color-scheme: light)">
	<img align="right" src="assets/preview/nitro-theme-light.png" alt="Nitro theme preview">
</picture>

1. Go to Settings > Plugins and enable the FakeNitro plugin.
2. Set corner smoothing to 0.1 in [Rounded Window Corners Reborn][ext-rounded-window-corners] extension settings.
3. Set a nitro theme in Settings > Display.

<br clear="right" />

### Transparent sidebar

<picture>
	<source srcset="assets/preview/transparent-sidebar-dark.png" media="(prefers-color-scheme: dark)">
	<source srcset="assets/preview/transparent-sidebar-light.png" media="(prefers-color-scheme: light)">
	<img align="right" src="assets/preview/transparent-sidebar-light.png" alt="Transparent sidebar preview">
</picture>

1. Get the [Blur my Shell][ext-blur-my-shell] extension
2. In the extension's settings, go to Pipelines > Manage Effects > Add the "Corner" effect. Click on the effect, set "Radius" to 17.

   The Adwaita window corner radius is 15, but setting it to said number will not _fully_ round them. 17 looks good on all windows.

   If the corners stick out, in [Rounded Window Corners Reborn][ext-rounded-window-corners] settings, turn up "Corner Smoothing".

3. In theme's [CSS file][css-main] set `--option-transparent-sidebar` to `true`.

Settings used for the screenshot were: radius - 100, brightness - 1.00.

<br clear="right" />

## Unsupported list

- Discord experiments

  I do not work for Discord, so I have no way of knowing if these experiments are getting changed, deprecated, etc.

- Nitro

  Exceptions — anything accessible with the FakeNitro plugin; it does support nitro themes after all.

[css-icons]: ./src/global/icons.scss
[css-main]: ./Discourse.theme.css
[ext-blur-my-shell]: https://github.com/aunetx/blur-my-shell
[ext-rounded-window-corners]: https://github.com/flexagoon/rounded-window-corners
[emoji-replace]: https://github.com/mwittrien/BetterDiscordAddons/tree/master/Themes/EmojiReplace/
