# Craft CMS + Twig Starter

This is a basic blog starter project for creating [Craft CMS](https://craftcms.com/) using the native [Twig](https://craftcms.com/docs/5.x/development/twig.html) templating language. It's a simple install that requires no database dump and no front-end tooling. It includes a single, first-party plugin ([CKeditor](https://plugins.craftcms.com/ckeditor)) to support a richer authoring experience.

## Features

- Dedicated places to edit global information and the primary top-level pages (_Home_, _Blog_, and _Guestbook_);
- _Blog_ and category feeds;
- Elegant content composition via CKEditor and nested entries;
- Front-end _Guestbook_ form, protected by login;
- Arbitrary _Pages_ structure for additional, hierarchical content;
- Preconfigured, [Craft Cloud](https://craftcms.com/cloud)-ready asset storage;

The Entries sidebar has also been configured to make these pages and sections easier to find for this setup.

## Installation

1. Clone this repository and move into the folder:

    ```bash
    git clone https://github.com/craftcms/starter-twig.git
    cd starter-twig/
    ```

2. Start DDEV:

    ```bash
    ddev start
    ```

3. Install dependencies:

    ```bash
    ddev composer install
    ```

4. Run the Craft setup wizard:

    ```bash
    ddev craft install
    ```

Congratulations—Craft has been installed! You can start exploring the control panel by visiting `https://starter-twig.ddev.site/admin` in your browser, or running `ddev launch admin`.

## Post-Install

### Control Panel

The Craft [control panel](https://craftcms.com/docs/5.x/system/control-panel.html) is available at `https://starter-twig.ddev.site/admin`. Log in with the username and password you created during installation!

- Create some content by visiting the **Entries** screen;
- Use Live Preview to visualize edits as you make them;
- Adjust or augment the content model by exploring the **Settings** screen;
- Open the front-end by clicking the site name in the upper-left corner;

> [!TIP]
> You can always get back to the control panel by appending `/admin` to the project’s base URL.

### Project Structure

This project was scaffolded from our blank-slate started kit, and therefore follows its overall [directory structure](https://craftcms.com/docs/5.x/system/directory-structure.html) and [configuration scheme](https://craftcms.com/docs/5.x/configure.html).

## Tips + Tricks

### Running on a Different Domain

The DDEV configuration files shipped with this project have a hard-coded project “name” that determines (among other things) the URL prefix. If you would like to change this (say, prior to pushing the project to a [new remote](#pushing-to-a-new-remote)), open `.ddev/config.yml` and update the `name` key.

Apply that change by running `ddev start` in the project directory. The site will restart, and be available at `https://{new-name}.ddev.site`!

### Pushing to a new Remote

When cloning a git repository, it typically sets up the origin as a default _remote_. To push the project to your own repository, follow these steps:

1. Remove the default origin:

    ```bash
    git remote remove origin
    ```

1. Create a new repository. This can be on GitHub, or any other git provider.
1. Add the new origin:

    ```bash
    git remote add origin https://github.com/your-username-or-org/new-repo-name.git
    ```

1. Push to the new origin:

    ```bash
    git push origin
    ```

> [!TIP]
> You may be able to create repositories in contexts that your local environment is not authorized to read from or write to! If you encounter permissions issues at this stage, consult the git provider’s documentation.

## Getting Help

If you have any questions or suggestions, you can always reach us at <support@craftcms.com> or [post a GitHub issue](https://github.com/craftcms/starter-twig/issues).

Thanks for trying Craft!

:lemon:
