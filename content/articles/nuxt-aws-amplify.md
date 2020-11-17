---
title: Deploying Serverless NUXT App with AWS Amplify
description: AWS Amplify, a faster, cheaper and better way to host your NUXT App
img: nuxt_amplify.png
alt: Creating my personal website with nuxt
---

# Creating My Personal Website

I wanted to create my personal website for quite sometime now. I have a [prior website](https://www.mohammadrafee.com), developed using [hugo](https://gohugo.io/). But, I wanted build something in a more hands-on fashion this time around. I have very limited experience with front-end. I still took it as a challenge to learn a front-end framework and how front-end frameworks work in general.

## Technologies

Learning something you never did before, is always daunting. I don't actually intend to be a front-end developer only in near future. However, it's always good to know, how things are handled in the front-end. Also, add it to the fact that, demand for full-stack developer outpaced the demand for simple front-end or back-end developer. From that perspective, learning a front-end framework seems like an worthwhile investment.

Once I decided to develop the app from scratch, the next question became the choice of technologies. Among all different front-end frameworks, Vue seemed like a rising star. It also seemed like the least daunting, compared to other frameworks. Others felt more difficult to grasp as beginner.

But Vue's choice of Single Page Application(SPA) model, although lucrative, left things to be desired. Also, the SPA model is not SEO friendly, which is important for a portfolio website. This is exactly, where NUXT came in. NUXT is a framework for Vue, to develop SEO friendly App, along with some additional features, that makes developing a Vue App, much simpler. So I decided to use NUXT developing front-end.

Now in terms of deploying the application, I ruled out something like NGINX soon. Hosting your own server, felt like too expensive for simple static sites. Amazon S3 offers static site hosting. Paired with Cloudfront, S3 offers excellent scalability and
