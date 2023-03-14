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

![1](https://t1283332.p.clickup-attachments.com/t1283332/77308b5c-0888-4d05-bf75-eff0034922a4/Screenshot%202023-03-14%20at%2011.33.49.jpg)
![2](https://t1283332.p.clickup-attachments.com/t1283332/a139be07-975b-4caa-adcc-3602b4a6c093/Screenshot%202023-03-14%20at%2011.33.58.jpg)

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
