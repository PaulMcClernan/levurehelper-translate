# translate Helper

The **translate** helper manages loading and retrieving strings in your user interface. Translations are stored as YAML files in a `./locales` folder. Each locale file should contain the same keys which you access using the `_t` function in your application. Using the `_t` function allows you to change the target locale in order to change the language of the stirngs that appear in your user interface.

## Contents

* [Activate the translate helper](#activate-the-translate-helper)
* [Configuration](#configuration)

## Activate the translate helper

To add the translate helper to your application you must download it and add the `translate` folder to your application `helpers` folder.

Click on the green **Clone or download** button on the GitHub page and select **Download ZIP** from the menu that appears. Grab the folder from the archive and rename it to `translate`. Add the renamed folder to your application `helpers` folder.

## Configuration

Locale files are YAML files stored in a `locales` folder that sits alongsde the `app.yml` file. You add a separate locale file for each language you want to support. A locale value contains key:value pairs.


### Example:
```
# ./locales/en.yml
greeting: Hi there!

# ./locales/fr.yml
greeting: Salut!

```
```
# Display "Hi there!" to the user
translateSetLocale "en"
answer _t("greeting")

# Display "Salut!" to the user
translateSetLocale "fr"
answer _t("greeting")
```
