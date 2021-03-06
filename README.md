# `angular-pane-manager-example`

There's currently a live demo of this project running [here](https://ryan-s.net/angular-pane-manager/)!

![screenshot](etc/screenshot.png)

This project shows off a simple example usage of [`angular-pane-manager`] and provides the Angular project scaffolding to build and publish the library.

`app.component.html` and `app.component.ts` show off some basics of the library, such as pane creation and layout save/restore.  `MotdComponent` and `EditorComponent` demonstrate writing components that support per-pane instancing with extra data and a customizable header.

## Getting Started

To get up and running for the first time, you will need to pull Git submodules and JS dependencies.  To do this, use the following two commands:

```sh
$ git submodule update --init --recursive
$ yarn install
```

And now, you should be able to run the project with `yarn start`.  If you have the Angular CLI installed, `ng serve` should also work.

The submodule `projects/angular-pane-manager` usually tracks the master branch of [`angular-pane-manager`], but you can verify this by checking the logs as follows:

```sh
$ cd projects/angular-pane-manager
$ git show -q HEAD
```

Git will indicate which branch the current HEAD of the submodule is tracking.

## Building and Running

To run the Webpack dev server, simply run `ng serve` or `yarn start`, and to build the project use `ng build` or `yarn build`.

To lint the project, run `./lint.sh`.  To run a production build of the project, run `./deploy.sh -n`, or `./deploy.sh -ln` to run a production build of the `angular-pane-manager` library.  For more info on these scripts you can run `./lint.sh -h` and `./deploy.sh -h`.

## Testing

To launch the unit test runner, use `ng test angular-pane-manager`.  Unit testing for `angular-pane-manager` is done with the default Karma and Jasmine setup, augmented with [`fast-check`] for running property tests, and [`chai`] for providing throwable assertions, which are required in order for `fast-check` to function properly.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

[`angular-pane-manager`]: https://github.com/openopus/ng-pane-manager2
[`fast-check`]: https://github.com/dubzzz/fast-check
[`chai`]: https://github.com/chaijs/chai
