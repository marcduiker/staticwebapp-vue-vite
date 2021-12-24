# Azure Static Web App Template with Node.js API

This is a template repository for Azure Static Web Apps that comes pre-configured with:

* [Vue.js v3](https://v3.vuejs.org/)
* [Vue Router v4](https://next.router.vuejs.org/)
* [Vuex v4](https://next.vuex.vuejs.org/)
* [A Node.js Azure Function](https://docs.microsoft.com/azure/static-web-apps/apis)
* [Vite.js](https://vitejs.dev/)

To install the dependencies run:

```shell
npm run init
```

To run the Static Web Apps Emulator:

1. Start the Vue front-end in the root:

    ```shell
    npm run dev
    ```

    > This should run the app on `http://localhost:3000/`.

2. Start the Node.js API (Azure Functions) in the `api` folder:

    ```shell
    cd api
    func start
    ```

    > This should run the API on `http://localhost:7071/`.

3. Finally start the Azure Static Web Apps CLI in the root:

    ```shell
     swa start http://localhost:3000 --api-location http://localhost:7071
    ```

    > This should run the Azure Static Web App on `http://localhost:4280`.
