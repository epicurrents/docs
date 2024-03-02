Requirements
============

## Browser compatibility

EpiCurrents is developed and tested in [Chromium-based](https://en.wikipedia.org/wiki/Chromium_(web_browser)) web browsers, namely Google Chrome and Microsoft Edge. Limited functionality may be available in other web browsers as well. EpiCurrents cannot be run in the Node.js environment.

## Cross-origin isolation

EpiCurrents makes use of JavaScript's SharedArrayBuffer and Atomics to reduce memory overhead when manipulating signals in web workers. If the hosting environment has not set up cross-origin isolation, the library will fall back to a worker-less operation mode that comes with a limited set features.

## Server requirements

Apart from static assets, EpiCurrents does not require anything from the hosting website and is run entirely on client side. Bundled code may require a specific directory structure for asynchronous code chunks and web workers to be loaded correctly.