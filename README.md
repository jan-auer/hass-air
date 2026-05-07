# Air

An Apple-inspired theme for Home Assistant, translated directly from the iOS 26 / iPadOS 26 design language into native HA CSS variables. No card-mod, no custom plugins — everything runs on pure theme YAML.

![Light mode]([docs/screenshot-light.png](https://github.com/user-attachments/assets/43e8e3c1-db8b-4e78-98ba-c9057e00ba3e))

![Dark mode]([docs/screenshot-dark.png](https://github.com/user-attachments/assets/b2978d6f-4c4d-49d1-906b-1aefa18afeda))

## Features

- Full light and dark mode with subtle gradient-mesh wallpapers
- Native `backdrop-filter` blur on app header and dialog surfaces
- iOS system tints across brand, state, weather, energy, and badge roles
- SF Pro on Apple devices; Inter / system-ui everywhere else
- Continuous-corner radius scale

## Installation

### HACS (recommended)

1. Open HACS → **⋮** → **Custom repositories**
2. Paste `https://github.com/jan-auer/hass-air` and set type to **Theme**, then click **Add**
3. Search for **Air** in HACS and click **Download**
4. Go to **Profile → Theme** and select **Air**

### Manual

1. Copy `themes/air.yaml` into your HA config's `themes/` folder
2. Add the following to `configuration.yaml` if not already present:
   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```
3. Restart Home Assistant
4. Go to **Profile → Theme** and select **Air**

### Default Theme

To set Air as the default for all users, call the **`frontend.set_theme`** action from **Developer Tools → Actions**:

```yaml
action: frontend.set_theme
data:
  name: Air
```

Home Assistant saves this setting and restores it on restart. Individual users can still override it from their own profile.

## Inspiration

Design tokens derived from Apple's iOS 26 Human Interface Guidelines and UIKit material specs.

## License

[MIT](LICENSE)
