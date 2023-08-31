---
layout: blog
title: Long running jobs
author: jay
image: assets/social-cards/sst-job.png
---

We launched a new construct that makes it easy to run functions longer than 15 minutes — [`Job`]({{ site.docs_url }}/long-running-jobs)

These are useful for cases where you are running async tasks like video processing, ETL, and ML. A `Job` can run for up to 8 hours.

`Job` is made up of:

1. [`Job`]({{ site.docs_url }}/constructs/Job) — a construct that creates the necessary infrastructure.
2. [`JobHandler`]({{ site.docs_url }}/packages/node#jobhandler) — a handler function that wraps around your function code in a typesafe way.
3. [`Job.run`]({{ site.docs_url }}/packages/node#jobrun) — a helper function to invoke the job.

## Launch event

We hosted a [launch livestream](https://www.youtube.com/watch?v=7sYdSbmi-ik) where we demoed the new construct, did a deep dive, and answered some questions.

<div class="youtube-container">
  <iframe src="https://www.youtube-nocookie.com/embed/7sYdSbmi-ik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

The video is timestamped and here's roughly what we covered.

1. Intro
2. Demo
3. Deep Dive
   - Deep dive into the construct
   - Granting permissions for running the job
   - Typesafety
   - Defining the job handler
   - Running the job
   - Live debugging the job
4. Q&A
   - Q: When should I use `Job` vs `Function`?
   - Q: Is `Job` a good fit for batch jobs?
   - Q: Why CodeBuild instead of Fargate?

## Get started

Here's how you use the new `Job` construct. Start by creating a new job.

```typescript
import { Job } from "@serverless-stack/resources";

const job = new Job(stack, "MyJob", {
  srcPath: "services",
  handler: "functions/myJob.handler",
});
```

Add the job handler.

```typescript
import { JobHandler } from "@serverless-stack/node/job";

declare module "@serverless-stack/node/job" {
  export interface JobTypes {
    MyJob: {
      foo: string;
    };
  }
}

export const handler = JobHandler("MyJob", async (payload) => {
  // Do the job
});
```

Finally invoke the job.

```typescript
import { Job } from "@serverless-stack/node/job";

function someFunction() {
  await Job.run("MyJob", {
    payload: {
      foo: "Hello World",
    },
  });
}
```

Note that the `payload` and job name `MyJob` here are typesafe.

For a full tutorial check out the [**Quick Start**]({{ site.docs_url }}/long-running-jobs#quick-start) in the docs.
