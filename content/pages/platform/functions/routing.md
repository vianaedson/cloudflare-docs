---
<<<<<<< HEAD
pcx-content-type: how-to
=======
pcx_content_type: how-to
>>>>>>> 070bee907 (Remove numbers from filename.)
title: Routing
weight: 4
---

# Functions routing
<<<<<<< HEAD
With Functions, users can take advantage of file-based routing where directory structure is mapped into routes. When you add a `functions` directory, you are indicating to Pages where you want the requests to be handled. For example, lets say you have `example.js` in the `functions` directory (`functions/example.js`). Requests to `/example` would be handled by the `example.js` file.

You can add multiple files or directories to your `functions` folder. You may write these files in either JavaScript (`*.js`) or TypeScript (`*.ts`). 

## Basic example 
For example, assume this simple directory structure:

    ├── ...
    ├── functions
    │     ├── example.js
    │     ├── example2.js
    │     ├── example3.js
    │     └── subfolder
              └──subthing.js
    └── ...

Then the directory structure will map to the following paths. 
    /example => /functions/example.js
    /example2 => /functions/example2.js
    /example3 => /functions/example3.js
    /subfolder/subthings => /functions/subfolder/subthings.js

## Dynamic paths
With Functions, you can also handle dynamic paths to allow matching on multiple paths without having to create a seperate file for each. There are two ways to make a dynamic path. Let's look at two examples to understand each.

Example 1: Single-path 

Example 2: Multi-path







=======

Using a `/functions` directory will generate a routing table based on the files present in the directory. You may use JavaScript (`*.js`) or TypeScript (`*.ts`) to write your Functions. A `PagesFunction` type is declared in the [@cloudflare/workers-types](https://github.com/cloudflare/workers-types) library which you can use to type-check your Functions.

For example, assume this directory structure:

    ├── ...
    ├── functions
    |   └── api
    │       ├── [[path]].ts
    │       ├── [username]
    │       │   └── profile.ts
    │       ├── time.ts
    │       └── todos
    │           ├── [[path]].ts
    │           ├── [id].ts
    │           └── index.ts
    └── ...

The following routes will be generated based on the file structure, mapping the URL pattern to the `/functions` file that will be invoked:

    /api/time => ./functions/api/time.ts
    /api/todos => ./functions/api/todos/index.ts
    /api/todos/* => ./functions/api/todos/[id].ts
    /api/todos/*/** => ./functions/api/todos/[[path]].ts
    /api/*/profile => ./functions/api/[username]/profile.ts
    /api/** => ./functions/api/[[path]].ts

## Path segments
>>>>>>> 070bee907 (Remove numbers from filename.)

In the [example above](/pages/platform/functions/#functions-routing):

- A `*` denotes a placeholder for a single path segment (for example, `/todos/123`).
- A `**` matches one or more path segments (for example, `/todos/123/dates/confirm`).

When naming your files:

- `[name]` is a placeholder for a single path segment.
- `[[name]]` matches any depth of route below this point.

{{<Aside type="note" header="Route specificity">}}

More specific routes (that is, those with fewer wildcards) take precedence over less specific routes.

{{</Aside>}}

When a filename includes a placeholder, the `name` must be alphanumeric and cannot contain spaces. In turn, the URL segment(s) that match the placeholder will be available under the `context.params` object using the filename placeholder as the key.
