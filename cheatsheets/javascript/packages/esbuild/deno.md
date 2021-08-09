---
title: Deno
description: How to use ESBuild in a Deno project
---


## Script

From the [docs](https://esbuild.github.io/getting-started/#deno).

- `build.ts`
    ```typescript
    import * as esbuild from 'https://deno.land/x/esbuild@v0.11.17/mod.js'

    const ts = 'let test: boolean = true'
    const result = await esbuild.transform(ts, { loader: 'ts' })

    console.log('result:', result)

    esbuild.stop()
    ```

Then run your script in the CLI.


## CLI

Note that the CLI tool is not available for use as a Deno package.

But you can install a binary using cURL and then use the package in the CLI, without needing Node or NPM.

See the [Download a binary][].

[Download a binary]: {{ site.baseurl }}{% cheatsheets/javascript/packages/esbuild/install.md#download-a-binary %}