<br/>
<div id="theia-logo" align="center">

    <h3>Online Customized IDE By Nitikesh</h3>
</div>

<div id="badges" align="center">

In this Application, we have used Theia Blue Print Open Source Platform and Docker for Permission management

</div>

## License

- [Eclipse Public License 2.0](LICENSE)
- [一 (Secondary) GNU General Public License, version 2 with the GNU Classpath Exception](LICENSE)


## Development

### Documentation

Documentation on how to package Theia as a Desktop Product may be found [here](https://theia-ide.org/docs/blueprint_documentation/)

### Repository structure

- Root level configures mono-repo build with lerna
- `applications` groups the different app targets
  - `electron` contains app to package, packaging configuration, and E2E tests for the electron target.
- `theia-extensions` groups the various custom theia extensions for Blueprint
  - `theia-blueprint-product` contains a Theia extension contributing the product branding (about dialogue and welcome page).
  - `theia-blueprint-updater` contains a Theia extension contributing the update mechanism and corresponding UI elements (based on the electron updater).

### Build

```sh
yarn
```

### Package the application

```sh
yarn electron package
```

The packaged application is located in `applications/electron/dist`.

### Create a preview application (without packaging it)

```sh
yarn electron package:preview
```

The packaged application is located in `applications/electron/dist`.

### Running E2E Tests

The E2E tests basic UI tests of the actual application.
This is done based on the preview of the packaged application.

```sh
yarn electron package:preview
yarn electron test
```

### Troubleshooting

>Inside your applciation folder
```

npm install electron --save
yarn theia start /my-container --hostname 0.0.0.0 --port 8080
```
