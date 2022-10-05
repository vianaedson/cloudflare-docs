---
pcx_content_type: get-started
title: Get started
weight: 1
---

# Get Started

## Powered by Cloudflare Workers

Cloudflare Workers is a [serverless platform](https://www.cloudflare.com/en-gb/learning/serverless/what-is-serverless/) that empowers you to run compute close to your users. Previously, you could only add dynamic functionality to your Pages site by manually deploying a Worker which meant that your application is deployed on top of both Pages and Workers. With Functions, you can leverage the Workers platform directly from within a Pages project. When you deploy a Function on Pages, it's just Workers under the hood!

## Setup
To get started, there are two ways to deploy a Function:
1. Create a `functions` directory at the root of your project backed by file-based routing. In doing this, Pages automatically generates a Function bundling the files in this folder. To get started this way, [follow this guide](/pages/platform/functions/first-function/).
2. Easily turn your Worker into a Function by providing it as a `_worker.js` in the output directory of your project. To begin with a Worker, [start here](<link>
