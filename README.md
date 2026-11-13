# Unraid templates

A collection of container templates for [Unraid](https://unraid.net).

## Available templates

- [m3u-editor](templates/m3u-editor.xml) - A powerful tool for managing and editing M3U playlists.
  - [https://m3ue.sparkison.dev](https://m3ue.sparkison.dev/)
- [nzbdavex](templates/nzbdavex.xml) - nzbdavex is a WebDAV proxy for NZB downloads. This version is a fork from the user Ghost which is focused on speed optimisations and other quality of life improvements.
  - [https://github.com/needforseed1/nzbdavex](https://github.com/needforseed1/nzbdavex)
- [arssra](templates/arssra.xml) - arssra is a powerful, lightweight service that bridges RSS feeds to Torznab APIs.
  - [https://github.com/dadarrs/arssra](https://github.com/dadarrs/arssra)

## Usage

### Community Applications (Recommended)

Requires the **Community Applications** plugin. Placing templates in CA's `private` directory lets Unraid generate `my-<name>.xml` in `templates-user/` on install without creating duplicate templates.

#### Using the Unraid terminal

Open the Unraid web terminal and run:

```bash
mkdir -p /boot/config/plugins/community.applications/private/dadarrs && wget -qO - https://github.com/dadarrs/unraid-templates/archive/refs/heads/main.tar.gz | tar xz -C /boot/config/plugins/community.applications/private/dadarrs --strip-components=2 unraid-templates-main/templates
```

Then open the **Apps** tab, select **Private Apps** in the left sidebar, and install the template you want.

#### Manual installation

1. Download the XML template you want to use.
2. Place it in a subfolder under `/boot/config/plugins/community.applications/private/` on your Unraid flash drive (for example, `/boot/config/plugins/community.applications/private/dadarrs/`).
3. Navigate to the **Apps** tab and select **Private Apps** in the left sidebar.
4. Click **Install** on the desired application.

> [!NOTE]
> If you do not use Community Applications and place a template directly into `/boot/config/plugins/dockerMan/templates-user/`, rename it to `my-<name>.xml` on initial install (and never overwrite an existing `my-<name>.xml`, as that holds your saved container configuration). If you previously installed unprefixed XML files into `templates-user/` and already have matching `my-<name>.xml` files, remove the unprefixed copies so Unraid does not read stale defaults when editing or updating.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
