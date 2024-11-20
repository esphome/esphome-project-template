# Repository Setup

- [ ] Replace the *.yaml files in the root of the repository with your project specific YAML configuration(s).
- [ ] `.github/workflows/publish-firmware.yml` 
    - [ ] `files` - Update YAML config filename(s).
    - [ ] `esphome-version` - Update ESPHome version.
    - [ ] `combined-name` - Update the combined name of the firmware. 
          Remove this line if you only target one microcontroller chip.
- [ ] `.github/workflows/ci.yml` 
    - [ ] `matrix` -> `file` - Update YAML config filename(s).
- [ ] `static/_config.yml` 
    - [ ] Set the title.
    - [ ] Set the description.
    - [ ] Optionally change the basic theme.
- [ ] `static/index.md` 
    - [ ] Update the manifest path. This will be `<combined-name>.manifest.json` if you use the `combined-name` in the publish-firmware.yml, otherwise it will be `<name>.manifest.json` where `<name>` is the value from `esphome` -> `name` in your YAML configuration.
    - [ ] Add some more content to the page.
- [ ] Set up GitHub Pages
    1. Go to **Repository Settings** -> **Pages** ([click here](../settings/pages)).
    2. Change the **Build and Deployment** -> **Source** to `GitHub Actions`.
- [ ] Make a [release](../releases/new) to trigger the first build and deploy the website.
