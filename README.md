# VueTorrent - Docker mod for qBittorrent 

This mod adds the [Vuetorrent](https://github.com/WDaan/VueTorrent) UI to qBittorrent. 
The UI is installed in `/app/vuetorrent`.

In qBittorrent docker arguments, set an environment variable `DOCKER_MODS=linuxserver/mods:qbittorrent-vuetorrent`

If adding multiple mods, enter them in an array separated by `|`, such as `DOCKER_MODS=linuxserver/mods:qbittorrent-vuetorrent|linuxserver/mods:qbittorrent-mod2`

By default the `latest` version is installed. To specify which release should be installed, environment variable `VUETORRENT_VERSION` can be used. E.g. `VUETORRENT_VERSION=v1.0.1`. The version specified must _exactly_ match one of the available [releases](https://github.com/WDaan/VueTorrent/releases), otherwise the installation will fail.

If at startup no `qBittorrent.conf` file exists yet (e.g. it is a fresh setup), the script will enable the alternative UI option and point the UI root path to `/app/vuetorrent`.
For pre-existing configurations, please add this path to your configuration.
