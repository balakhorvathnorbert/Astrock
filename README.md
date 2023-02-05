# deno-fresh-template

- Follow the commands to bootstrap your [Deno](https://deno.land/) project with [Fresh](https://fresh.deno.dev/) framework:

    ``` shell
    deno run -A -r https://fresh.deno.dev my-project
    cd my-project
    deno task start
    ```

- In `./main.ts`, add `port: Deno.env.get("PORT")` to the `start` function and listen to the custom port given the `.env` file

    ```typescript
    start(manifest, { plugins: [twindPlugin(twindConfig)], port: Deno.env.get("PORT")}, );
    ```

- To run locally, copy `.env.defaults` to a new file `.env`, and modify `.env` by assigning the port that you would like to run your application.

    ```shell
    cp .env.defaults .env
    ```

    ```shell
    # in .env
    PORT=<your port>
    ```

- **Do not** add `fresh.gen.ts` to your `.gitignore` file.
