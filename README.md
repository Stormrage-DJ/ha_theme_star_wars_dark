# Star Wars Dark Theme
Star Wars The Old Republic inspired Dark theme for Home Assistant

## Screenshots
![](https://raw.githubusercontent.com/Stormrage-DJ/ha_theme_star_wars_dark/main/docs/swd_01.png)
![](https://raw.githubusercontent.com/Stormrage-DJ/ha_theme_star_wars_dark/main/docs/swd_02.png)
![](https://raw.githubusercontent.com/Stormrage-DJ/ha_theme_star_wars_dark/main/docs/swd_03.png)

## Preparation
1. Make sure that under the **configuration.yaml** file you have the following:

```
frontend:
  themes: !include_dir_merge_named themes
```

2. Under the Home Assistant **Config** folder, create a new folder named **themes**
3. **Restart** Home assistant to apply the changes. 

### HACS installation
1. Go into the Community Store (HACS)
2. Search for **Star Wars Dark**
3. Open the theme
4. Press Install
5. Restart Home Assistant

### Manual installation
1. In the Home assistant **themes** folder, create a file named `star_wars_dark.yaml`
2. In this GitHub repo, go into the **themes** folder, open the `star_wars_dark.yaml` file and copy the content
3. Paste the content in the `star_wars_dark.yaml` file created under your Home Assistant themes folder

### (Optional) Local hosted background file (if your HA does not have internet access)
1. Add allowed external directory to your `configuration.yaml`
```
homeassistant:
  allowlist_external_dirs:
    - "/config/www"
```
2. Copy the `star_wars_dark_bg.png` from your `themes` folder to `/www/images/`
3. In the file named `star_wars_dark.yaml` search for `card-mod-view` section and replace the url with `/local/images/star_wars_dark_bg.png`.
4. Restart Home Assistant to apply configuration changes and to load the folder contents

### Enable theme
1. Open your Home Assistant **Profile**
2. Under, **Themes**, select the new **Star Wars Dark**

### Set theme as default for all devices
1. Open **Developer Tools**
2. Go to **Services**
3. Under **Service** enter `frontend.set_theme`
4. Under **Name**, enter `Star Wars Dark`
5. Enable **Mode** and set it to `light`
6. Click on **Call Service**
7. Repeat steps 1 to 6 but change the **Mode** to `dark`
