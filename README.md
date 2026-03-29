# Fluxer

Fluxer is a free and open-source instant messaging and voice-over-IP application. It provides text chat, voice calls, video calls, and screen sharing in a modern interface.

This repo hosts the flatpak manifest for [Fluxer, available at Flathub](https://flathub.org/en/apps/app.fluxer.Fluxer).

```bash
flatpak install app.fluxer.Fluxer
flatpak run app.fluxer.Fluxer
```

### Persistent flags

To make Fluxer's launch flags persistent, add them to `~/.var/app/app.fluxer.Fluxer/config/fluxer-flags.conf` (one option per line):

```
# This is just an example
--ozone-platform-hint=auto
# This line will be ignored
--enable-features=WaylandWindowDecorations

```

### File Access

Default flatpak permissions for this package limit Fluxer to only certain directories, so you can't access your entire Home directory. Currently, this limits which file directories you can attach files from and impacts drag and drop functionality.

To work around this now, you can use the file picker via `Upload File` option in fluxer or change flatpak permissions for fluxer (for example, with [Flatseal](https://flathub.org/en/apps/com.github.tchx84.Flatseal) or with flatpak override --user --filesystem=home app.fluxer.Fluxer) to give Fluxer access to the specified directory, allowing drag and drop file attachments from more locations.

### Reporting bugs

If you're experiencing a problem exclusive to the Flatpak version of Fluxer, i.e. it doesn't happen when running Fluxer unsandboxed (AppImage, RPM, DEB, etc), feel free to open an issue about it here.

Otherwise, open an issue in the [upstream repository](https://github.com/fluxerapp/fluxer.git).

If you need help troubleshooting or have suggestions related to the Flatpak version, you can join the [Fluxer Developers](https://fluxer.gg/fluxer-developers) community and discuss them in the [`#flatpak`](https://web.fluxer.app/channels/1427764813854588940/1474436641954701476) channel.
