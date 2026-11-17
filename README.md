# Eggs for Axolotl-PM

Eggs that install and run [Axolotl-PM](https://github.com/axolotl-pm), a fork of PocketMine-MP, on game server panels.

There is one egg per panel. Pick the one that matches your panel:

| Panel | Egg |
|---|---|
| [Pelican](https://pelican.dev) | [egg-pelican-axolotl--p-m.json](./egg-pelican-axolotl--p-m.json) |
| [Pterodactyl](https://pterodactyl.io) | [egg-pterodactyl-axolotl--p-m.json](./egg-pterodactyl-axolotl--p-m.json) |

The two eggs install the same thing. They differ only in the file format and the panel-specific values (Docker images, port placeholder and so on) each panel expects.

## Usage

### Pelican

1. In the admin panel, open **Eggs** and click **Import**.
2. Import [egg-pelican-axolotl--p-m.json](./egg-pelican-axolotl--p-m.json), either by uploading the file or from this URL:
   `https://raw.githubusercontent.com/axolotl-pm/egg/master/egg-pelican-axolotl--p-m.json`
3. Create a server that uses the new egg.

### Pterodactyl

1. In the admin panel, open **Nests**, choose a nest (for example Minecraft) and click **Import Egg**.
2. Upload [egg-pterodactyl-axolotl--p-m.json](./egg-pterodactyl-axolotl--p-m.json) and select the nest.
3. Create a server that uses the new egg.

## Versions

The **Version to install** variable chooses the PHP version that Axolotl-PM runs on.

| Value | PHP |
|---|---|
| `PM5PHP82` | 8.2 |
| `PM5PHP83` | 8.3 |
| `PM5PHP84` (default) | 8.4 |
| `PM5PHP85` | 8.5 |

Prebuilt PHP binaries are downloaded from [axolotl-pm/PHP-Binaries](https://github.com/axolotl-pm/PHP-Binaries) on x86_64. On ARM64 there are no prebuilt binaries, so PHP is compiled during installation, which takes a long time.

The version is only read during installation. To change it on an existing server, change the variable and reinstall the server.

## Updating

Both eggs carry an update URL that points at this repository. Pelican uses it to update an imported egg from the panel. On Pterodactyl, import the new file again to update the egg.
