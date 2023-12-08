NOTE: issue and solution outline here: https://github.com/vuejs/vue-cli/issues/6345

To Repro:

- clone this repo

To confirm that vue-lib works properly when run as an application

- cd vue-lib-bug-repro/vue-lib
- npm i
- npm run build-lib
- npm run serve

You should see the following:

<img width="243" alt="Screenshot 2023-12-08 at 5 20 29 AM" src="https://github.com/luetkemj/vue-lib-bug-repro/assets/925980/bdcceaf5-e317-425a-9741-f418ba73de7d">

To repro that vue-lib does not work properly when use as a library

- cd vue-lib-bug-repro/vue-app
- npm i
- npm run serve

You should see the following incorrect result:

<img width="262" alt="Screenshot 2023-12-08 at 5 19 52 AM" src="https://github.com/luetkemj/vue-lib-bug-repro/assets/925980/b1b2cb89-f193-4ffd-9583-a75e3af6b607">

Notice how in the second example, the imported "DsiWorld" component does not render when used in the "DsiHello" component but does render when used by itself.

In dev tools you can see that the component is being output as raw html instead of as a compiled vue component.

<img width="379" alt="Screenshot 2023-12-08 at 5 30 17 AM" src="https://github.com/luetkemj/vue-lib-bug-repro/assets/925980/380028cf-71b1-43df-8e24-3011ae2499bd">
