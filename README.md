# shopify-env-local

Required packages:

-   [env-cmd](https://www.npmjs.com/package/env-cmd) `npm install -g env-cmd`
-   [shopify-cli](https://shopify.dev/docs/themes/tools/cli/install)
    -   windows/linux:
        -   `npm install -g @shopify/cli @shopify/theme`
    -   mac:
        -   `brew tap shopify/shopify`
        -   `brew install shopify-cli`

Required Shopify App:

-   [Theme Access](https://apps.shopify.com/theme-access) by Shopify

First add the Theme Access app to the site. Then add the developer in question to it.

The developer will get an email to "Get password", with this information we can create or `.env` file

```
SHOPIFY_FLAG_STORE=store-name.myshopify.com
SHOPIFY_CLI_THEME_TOKEN=shptka_xxx000xxx000xxx00xxx000xxx000xxx
```

NOTE:

Replace `store-name` with the store handle

Replace `shptka_xxx000xxx000xxx00xxx000xxx000xxx` with the password provided by the app.

**NOTE2**:

Remember adding a `.gitignore` file with the next lines

.env
.shopifyignore

And `.shopifyignore` file with the next data

.env
.gitignore

Since this `.env` file contains sensitive information it should never be pushed to any repo.

Documentation:

<https://shopify.dev/docs/themes/tools/cli/ci-cd#step-2-integrate-shopify-cli-into-your-pipeline>
