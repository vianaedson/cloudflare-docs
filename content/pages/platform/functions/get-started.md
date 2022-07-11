---
<<<<<<< HEAD
pcx-content-type: get-started
=======
pcx_content_type: get-started
>>>>>>> 070bee907 (Remove numbers from filename.)
title: Get started
weight: 1
---

# Get Started

<<<<<<< HEAD
## Powered by Cloudflare Workers

Cloudflare Workers is a [serverless platform](https://www.cloudflare.com/en-gb/learning/serverless/what-is-serverless/) that empowers you to run compute close to your users. Previously, you could only add dynamic functionality to your Pages site by manually deploying a Worker which meant that your application is deployed on top of both Pages and Workers. With Functions, you can leverage the Workers platform directly from within a Pages project. When you deploy a Function on Pages, it's just Workers under the hood!

## Setup
To get started, there are two ways to deploy a Function: 
1. Create a `functions` directory at the root of your project backed by file-based routing. In doing this, Pages automatically generates a Function bundling the files in this folder. To get started this way, [follow this guide](/pages/platform/functions/first-function/). 
2. Easily turn your Worker into a Function by providing it as a `_worker.js` in the output directory of your project. To begin with a Worker, [start here](<link> 
=======
## Built with Cloudflare Workers

Cloudflare Workers provides a serverless [execution environment](https://www.cloudflare.com/en-gb/learning/serverless/what-is-serverless/) that allows you to create entirely new applications or augment existing ones without configuring or maintaining infrastructure.

Previously, you could only add dynamic functionality to your Pages site by manually deploying a Worker using Wrangler, which meant that your application is written across both Pages and Workers. 

Functions allow you to leverage the Workers platform directly from within a Pages project by utilizing a project's filesystem convention. In addition, Functions enable you to deploy your entire site – static and dynamic content – when you `git push`.

{{<Aside type="note" header="Functions is currently in beta">}}
You can track current issues that the Pages team is fixing in Known issues. Let us know any unreported issues by posting in the Cloudflare Developers Discord.
{{</Aside>}}

## Setup

To get started, create a `/functions` directory at the root of your project. Writing your Functions files in this directory automatically generates a Worker with custom functionality at the predesignated routes.

Now that you have your `/functions` directory setup, get started [writing your first function](/pages/platform/functions/first-function/)

## Demo

To get started with your first Pages project with Functions, refer to the [demo blog post on how to build an image sharing application](http://blog.cloudflare.com/building-full-stack-with-pages). In this demo, you will build a JSON API with Functions (storing data on KV and Durable Objects), integrate with [Cloudflare Images](/images/) and [Cloudflare Access](/cloudflare-one/), and use React for your front end.
>>>>>>> 070bee907 (Remove numbers from filename.)
