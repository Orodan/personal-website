---
title: Creating my personal website with nuxt
description: Ever wonder how to build you own personal site with Nuxt ? This blog post is for you ! A simple tour of what I've used in Nuxt and my opinion on them after this experience.
img: nuxt-icon.png
alt: Creating my personal website with nuxt
---

# Creating my personal website with nuxt

Welcome to my first blog post using the content module offered by nuxt ! In this post I'll describe my first real experience with Nuxt.

## The project

First, the project. My project was something I had in mind for a long time, but never managed to find the time to do : a simple personal website to gain visibility on the web and show a bit of what I do. The confinement in France had one positive impact on me : I got started with this project. I had a rough idea of what I wanted in this website : a resume of what my work experiences and skills ; a list of way to contact me and a blog section where I could start writing.

## Why Nuxt ?  

One thing to know about me is I love front end development. I already have a bit of real world experiences with Angular and React, so I wanted to try Vue on a real project which goes a bit beyond classical tutorials (big fan of learn by doing). At the same time, I knew I wasn't good enough with Vue to create alone a 
whole project structure from scratch (and not regret it later at least). And here come Nuxt and the very first advantage I saw in this framework. Starting a project with Nuxt is very simple and it takes care for you of the pain of all the set up pain. It allowed me to focus on developing and creating content from the get-go. I also knew a bit about what Nuxt opinions and features were so I knew I could make my project with it.

## Feedback on ?  

Now that we know why Nuxt, it's time to dive into what I used in Nuxt. Keep in mind it's opiniated list of some of the main stuff I used. Nuxt is much richer than just that.  

<br/>

### Dynamic routing  

<br/>

Do you remember php ? Yes I just said php, please do not be afraid. Nuxt proposes a routing system very similar to what php proposed : based of file names and directory structures. Everything starts with the *pages* directory. Inside, you will place your pages (no kidding). By pages, I mean Vue components linked to a route. But how do I define these routes ? You don't ! When Nuxt builds your project, it looks at the files inside your *pages* directory and generate it for you, based on the names you gave to your files.

<br/>

### Layout
<br/>

Layout allows you to easily configure to configure the aspect of your app. It places itself one step higher than the pages. In my case, I used it in a very simple way : to display components common to every page without repeting myself :

<br/>

```js
<Header />

<Nuxt />

<Footer />
```
<br/>

The `<Nuxt />` represents the page you're in, depending on your app and current route. It's only one use case of Nuxt layouts, you can easily find more use cases on the Nuxt documentation, such as creating a specific layout according to the resolution (mobile/tablet/desktop) for example.

<br/>

### Static mode
<br/>

One of my favorite feature so far ! I knew my personal website - at least in a first version - did not need to request any apis at runtime to display my content. So all my content could be generated at build time. But how could I take advantage of that ? Well the Nuxt static mode does the exact job ! It goes through all your pages and generate all your content, at build time. It also means I could use a static hosting services such as Netlify to host my site.

<br/>

### Nuxt content
<br/>

In my personal website, I wanted one specific feature : the ability to easily write and display blog posts. To do so, I tried one of the latest Nuxt module : @nuxt/content. 

To install this module, it has been as easy as :

<br/>

```
npm install @nuxt/content
```
<br/>

and add the new module in nuxt.config.js :

<br/>

```js
{
   modules: [
      '@nuxt/content'
   ],
}
```
<br/>

Ok so at this point, the @nuxt/content module is installed. What's next ? Well creating your content. All you have to do is create files in a content directory. @nuxt/content supports all kind of formats (markdown, json, csv, xml). I personally went with markdown as it is a format I'm confortable with. Another thing to note is that, in addition to your content, you can add metadata to your content file. In my case, I added a title, a description and an image.

<br/>

Last step : how to I display the content I just created. First, you got to fetch it. For that, I used the asyncData method available of all pages of a Nuxt app. This method is called when navigating to the matching route and before initializing the component. In this method, you have access to a context object. By adding the @nuxt/content module, this context object is enriched  with a $content property which will help us interact with our content. To fetch a content, it looks like this :

<br/>

```js
const article = await $content('articles', params.slug).fetch()

return { article }
```

<br/>

The parameters define the path of the content you're looking for. If no parameters are defined, tt defaults to the root of the content directory of your app. In my case, I created an articles subdirectory to organize my content. So I'm asking for the content inside a subdirectory called articles and named as the slug parameter in my current url.

<br/>

## What I appreciated the most ?

I appreciated a lot the simplicity of working with Nuxt. No time lost on complex configuration or importing a number of libraries. You just get a concise, easy-to-read and working architecture and configuration from the get-go, allowing you to work on your ideas and your content. This also works very well thanks to the clarity of the documentation and the great articles you can find on the nuxt blog section. Big thumb up for that :)


## The biggest struggle I had ?

The biggest struggle I faced on this project was about loading images. I decided to associate an image to every article I'll write. For the article you're currently reading, my first reflex was to add the image to the assets folder, like every other images of this site. But my image was never found. It turns out, the difference between this image and the other was that my image was loaded dynamically, according to the metadata of the article you're on.

<br/>

```js
<img :src="articleSummary.img" :alt="articleSummary.title" />
```

<br/>

Because of that, when Webpack bundles your app, it can not determine that this particular image in your asset is being used. Indeed, it never found an explicit use of it in your app at build time. So it removes it from your final bundle ! I found a simple way to solve it : instead of placing my image in the assets folder, I put it in the static folder. The content in this folder is always part of your final bundle, without build time analysis. I hope this explanation will save save you some struggle time if you meet the same issue.

## Conclusion


