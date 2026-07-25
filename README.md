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

### The easy way (Unraid terminal)

Since the "Template repositories" text box was removed in Unraid 6.10, the easiest way to add these templates is via the Unraid terminal. 

Open the Unraid web terminal and run the following command to download all templates automatically:

```bash
wget -qO - https://github.com/dadarrs/unraid-templates/archive/refs/heads/main.tar.gz | tar xz -C /boot/config/plugins/dockerMan/templates-user/ --strip-components=2 unraid-templates-main/templates
```

Once downloaded, navigate to the **Docker** tab, scroll to the bottom, click **"Add Container"**, and select the template from the **"Template"** drop-down.

### The manual way

1. Download the XML template you want to use.
2. Place it in `/boot/config/plugins/dockerMan/templates-user/` on your Unraid flash drive.
3. Navigate to the **Docker** tab, scroll to the bottom, and click **"Add Container"**.
4. Select the template's name from the **"Template"** drop-down.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
