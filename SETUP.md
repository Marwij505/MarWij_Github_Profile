# Profile setup & maintenance

## Display this README on your GitHub profile

GitHub displays a profile README only when a **public repository has the same name as your username** and contains a non-empty `README.md` in its root.

Your profile repository must therefore be **Marwij505/Marwij505**. This checkout currently points to **Marwij505/MarWij_Github_Profile**, which does not activate the profile README.

Choose one approach:

1. Rename the current GitHub repository to `Marwij505` in its repository settings, then update the local remote:

   ```sh
   git remote set-url origin https://github.com/Marwij505/Marwij505.git
   ```

2. Keep this repository as the source and create a separate public repository named `Marwij505`. Copy `README.md` and the entire `assets/` directory into that repository's root.

Commit and push the profile files to the chosen repository's default branch. Open [your GitHub profile](https://github.com/Marwij505) and verify the banner, project links, light/dark appearance, and contact links.

No website hosting, API tokens, scheduled workflows, or external image services are needed.

Reference: [GitHub's profile README requirements](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme).

## Suggested sidebar profile

The README does not change GitHub's sidebar fields. In **Edit profile**, use:

- **Name:** Marcell Juniar Wijaya
- **Bio:** Informatics student exploring software engineering, applications, data, and IT. Building practical solutions with curiosity and continuous learning.
- **Location:** Bekasi, Indonesia
- **Website:** https://marwij505.github.io/
- **LinkedIn:** https://www.linkedin.com/in/marcell-wijaya/

Suggested pinned repositories, in order:

1. `bakery_store` — business operations and relational data.
2. `help_desk` — information systems and educational support.
3. `task_management_laravel` — workflows and application structure.
4. `marcell-wijaya_kelompok-5_kh002` — Flutter and Dart coursework.

## Design & motion

- Native Markdown and simple HTML keep the text selectable and the links accessible.
- Local SVG banners provide light and dark versions, with slow orbit, line movement, and opacity transitions.
- No JavaScript, embedded website, or page-level CSS is required. GitHub sanitizes README HTML, so website-style hover/scroll transitions are not part of this design.
- Reduced-motion picture sources and an SVG media query provide a static experience where the viewer supports those preferences.
- If you want static banners for everyone, change the two animated image references in the README to their `-static.svg` equivalents.
- Theme selection follows the viewer's supported color-scheme preference. Verify it on GitHub after publishing, particularly when the site theme differs from the operating-system theme.
- The banner is decorative: your name, background, project descriptions, and contact information remain readable in the README without images.

## Update the assets

Edit `scripts/build_assets.py`, then regenerate the four SVGs:

```sh
python scripts/build_assets.py
```

The generator uses only Python's standard library. Commit the generated SVGs along with the script so GitHub can display them directly.

The README image URLs include a version parameter (currently `?v=2`). After changing a banner, increment this value on all four image references and commit the README alongside the assets. This gives the updated images new URLs when a browser or image cache still serves the previous version.

## Content grounding

The project descriptions were checked against public repository READMEs and source structure on October 11, 2026:

- [Bakery Store](https://github.com/Marwij505/bakery_store): Flask, MySQL, product management, and management roles.
- [Compass Campus](https://github.com/Marwij505/help_desk): educational help desk; explicitly in development.
- [Flowlist](https://github.com/Marwij505/task_management_laravel): Laravel task management, calendar, statistics, profiles, and MySQL.
- [Mobile coursework](https://github.com/Marwij505/marcell-wijaya_kelompok-5_kh002): Flutter/Dart layouts, profile cards, themes, and reusable widgets.

Broader software engineering, data analysis, automation, and IT work are described as interests or learning directions, not employment history or professional certifications. No unverified project metrics are displayed.

`campus_app` was visible in the supplied screenshot but unavailable through the connected GitHub repository API. It is not included in the public project selection. `Simple_radar` was not selected because its inspected implementation file was empty.
