# nx-26041

## Steps

1. Check out the repo on the `main` branch and run `npm install`.

1. Make a change to button and commit it locally.

   <img width="1177" alt="image" src="https://github.com/JamesHenry/nx-26041/assets/900523/66877421-8139-4782-ab4a-a885961d258c">

1. Run a dry-run of `nx release` and verify the output

```sh
❯ nx release -d                                                                                                                         

 NX   Running release version for project: @org/myproject-otherpackage1

@org/myproject-otherpackage1 🔍 Reading data for package "@org/myproject-otherpackage1" from packages/otherpackage-1/package.json
@org/myproject-otherpackage1 📄 Resolved the current version as 0.1.2 from git tag "@org/myproject-otherpackage1@0.1.2".
@org/myproject-otherpackage1 🚫 No changes were detected using git history and the conventional commits standard.
@org/myproject-otherpackage1 🚫 Skipping versioning "@org/myproject-otherpackage1" as no changes were detected.

 NX   Running release version for project: @org/myproject-otherpackage2

@org/myproject-otherpackage2 🔍 Reading data for package "@org/myproject-otherpackage2" from packages/otherpackage-2/package.json
@org/myproject-otherpackage2 📄 Resolved the current version as 0.3.4 from git tag "@org/myproject-otherpackage2@0.3.4".
@org/myproject-otherpackage2 🚫 No changes were detected using git history and the conventional commits standard.
@org/myproject-otherpackage2 🚫 Skipping versioning "@org/myproject-otherpackage2" as no changes were detected.

 NX   Running release version for project: @org/myproject-button

@org/myproject-button 🔍 Reading data for package "@org/myproject-button" from packages/button/package.json
@org/myproject-button 📄 Resolved the current version as 1.0.0 from git tag "@org/myproject-button@1.0.0".
@org/myproject-button 📄 Resolved the specifier as "minor" using git history and the conventional commits standard.
@org/myproject-button ✍️  New version 1.1.0 written to packages/button/package.json

 NX   Running release version for project: @org/myproject-datepicker

@org/myproject-datepicker 🔍 Reading data for package "@org/myproject-datepicker" from packages/datepicker/package.json
@org/myproject-datepicker 📄 Resolved the current version as 1.2.3 from git tag "@org/myproject-datepicker@1.2.3".
@org/myproject-datepicker 📄 Resolved the specifier as "patch" because "release.version.generatorOptions.updateDependents" is enabled
@org/myproject-datepicker ✍️  New version 1.2.4 written to packages/datepicker/package.json

 NX   Running release version for project: @org/myproject-dropdown

@org/myproject-dropdown 🔍 Reading data for package "@org/myproject-dropdown" from packages/dropdown/package.json
@org/myproject-dropdown 📄 Resolved the current version as 4.5.6 from git tag "@org/myproject-dropdown@4.5.6".
@org/myproject-dropdown 📄 Resolved the specifier as "patch" because "release.version.generatorOptions.updateDependents" is enabled
@org/myproject-dropdown ✍️  New version 4.5.7 written to packages/dropdown/package.json

 NX   Running release version for project: @org/myproject-filter

@org/myproject-filter 🔍 Reading data for package "@org/myproject-filter" from packages/filter/package.json
@org/myproject-filter 📄 Resolved the current version as 7.8.9 from git tag "@org/myproject-filter@7.8.9".
@org/myproject-filter 📄 Resolved the specifier as "patch" because "release.version.generatorOptions.updateDependents" is enabled
@org/myproject-filter ✍️  New version 7.8.10 written to packages/filter/package.json

 NX   Running release version for project: @org/myproject-modal

@org/myproject-modal 🔍 Reading data for package "@org/myproject-modal" from packages/modal/package.json
@org/myproject-modal 📄 Resolved the current version as 10.11.12 from git tag "@org/myproject-modal@10.11.12".
@org/myproject-modal 📄 Resolved the specifier as "patch" because "release.version.generatorOptions.updateDependents" is enabled
@org/myproject-modal ✍️  New version 10.11.13 written to packages/modal/package.json

UPDATE packages/button/package.json [dry-run]

    "name": "@org/myproject-button",
-   "version": "1.0.0"
+   "version": "1.1.0"
  }

UPDATE packages/datepicker/package.json [dry-run]

    "name": "@org/myproject-datepicker",
-   "version": "1.2.3",
+   "version": "1.2.4",
    "dependencies": {
-     "@org/myproject-button": "1.0.0"
+     "@org/myproject-button": "1.1.0"
    }

UPDATE packages/dropdown/package.json [dry-run]

    "name": "@org/myproject-dropdown",
-   "version": "4.5.6",
+   "version": "4.5.7",
    "dependencies": {
-     "@org/myproject-button": "1.0.0"
+     "@org/myproject-button": "1.1.0"
    }

UPDATE packages/filter/package.json [dry-run]

    "name": "@org/myproject-filter",
-   "version": "7.8.9",
+   "version": "7.8.10",
    "dependencies": {
-     "@org/myproject-button": "1.0.0"
+     "@org/myproject-button": "1.1.0"
    }

UPDATE packages/modal/package.json [dry-run]

    "name": "@org/myproject-modal",
-   "version": "10.11.12",
+   "version": "10.11.13",
    "dependencies": {
-     "@org/myproject-button": "1.0.0"
+     "@org/myproject-button": "1.1.0"
    }


 NX   Updating npm lock file


 NX   Staging changed files with git


 NX   Previewing an entry in packages/datepicker/CHANGELOG.md for @org/myproject-datepicker@1.2.4


CREATE packages/datepicker/CHANGELOG.md [dry-run]
+ ## 1.2.4 (2024-06-09)
+
+
+ ### 🧱 Updated Dependencies
+
+ - Updated @org/myproject-button to 1.1.0


 NX   Previewing an entry in packages/dropdown/CHANGELOG.md for @org/myproject-dropdown@4.5.7


CREATE packages/dropdown/CHANGELOG.md [dry-run]
+ ## 4.5.7 (2024-06-09)
+
+
+ ### 🧱 Updated Dependencies
+
+ - Updated @org/myproject-button to 1.1.0


 NX   Previewing an entry in packages/button/CHANGELOG.md for @org/myproject-button@1.1.0


CREATE packages/button/CHANGELOG.md [dry-run]
+ ## 1.1.0 (2024-06-09)
+
+
+ ### 🚀 Features
+
+ - a change to button
+
+
+ ### ❤️  Thank You
+
+ - “JamesHenry”


 NX   Previewing an entry in packages/filter/CHANGELOG.md for @org/myproject-filter@7.8.10


CREATE packages/filter/CHANGELOG.md [dry-run]
+ ## 7.8.10 (2024-06-09)
+
+
+ ### 🧱 Updated Dependencies
+
+ - Updated @org/myproject-button to 1.1.0


 NX   Previewing an entry in packages/modal/CHANGELOG.md for @org/myproject-modal@10.11.13


CREATE packages/modal/CHANGELOG.md [dry-run]
+ ## 10.11.13 (2024-06-09)
+
+
+ ### 🧱 Updated Dependencies
+
+ - Updated @org/myproject-button to 1.1.0


 NX   Staging changed files with git


 NX   Committing changes with git


 NX   Tagging commit with git


 NX   Skipped publishing packages.


NOTE: The "dryRun" flag means no changes were made.
```
