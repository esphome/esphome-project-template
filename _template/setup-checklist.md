# Repository Setup

- [ ] Replace the *.yaml files in the root of the repository with your project specific YAML configuration(s).
- [ ] `.github/workflows/build.yml`
    - [ ] `combined-name` - Update the combined name of the firmware.
          Remove this line if you only target one microcontroller chip.
    - [ ] `esphome-version` - Update ESPHome version.
- [ ] `static/_config.yml`
    - [ ] Set the title.
    - [ ] Set the description.
    - [ ] Optionally change the basic theme.
- [ ] `static/index.md`
    - [ ] Update the manifest path. This will be `<combined-name>.manifest.json` if you use the `combined-name` in the build.yml, otherwise it will be `<name>.manifest.json` where `<name>` is the value from `esphome` -> `name` in your YAML configuration.
    - [ ] Add some more content to the page.
- [ ] Set up GitHub Pages
    1. Go to **Repository Settings** -> **Pages** ([click here](../settings/pages)).
    2. Change the **Build and Deployment** -> **Source** to `GitHub Actions`.
- [ ] Make your first release
    1. Push your configuration changes to the `main` branch. The **Release Drafter** workflow creates a draft release and the **Build** workflow attaches the firmware to it.
    2. Wait for the **Build** workflow to finish and remove the "DO NOT PUBLISH THIS RELEASE YET" notice from the draft.
    3. Once the notice is gone, run the **Release** workflow (**Actions** -> **Release** -> **Run workflow**) to publish the draft and deploy the website.
