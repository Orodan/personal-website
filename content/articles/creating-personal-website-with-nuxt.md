---
title: Creating my personal website with Nuxt.js
description: Ever wonder how to build you own personal site with Nuxt ? This blog post is for you ! A simple tour of what I've used in Nuxt and my opinion on them after this experience.
img: nuxt-icon.png
alt: Creating my personal website with nuxt
---

# Creating my personal website with Nuxt.js

Welcome to my first blog post using the content module offered by Nuxt.js! In this post I'll describe my first real experience with Nuxt.js creating my personal website.

## The project

First, the project. My project was something I had in mind for a long time, but never managed to find the time to do: a simple personal website to gain visibility on the web and show a bit of what I do. Thanks to the lockdown in France I got started with this project. I had a rough idea of what I wanted in this website: a summary of what I do, my work experiences and skills; the different ways to contact me and a blog section where I could start writing.

<div class="article-image-container">
  <img src="/site-combined.png">
</div>

## Why Nuxt.js?

One thing to know about me is that I love front-end development. I already have a bit of real-world experiences with Angular and React, so I wanted to try Vue.js on a real project which goes a bit beyond classical tutorials (being a big fan of learning by doing). At the same time, I knew I wasn't good enough with Vue.js to create a whole project structure from scratch (without regretting it later at least). And here comes Nuxt.js and the very first advantage I saw in this framework. Starting a project with Nuxt.js is very simple and it takes care of all the set up pain for you. It allowed me to focus on developing and creating content from the get-go. I also knew a bit about what Nuxt.js opinions and features were so I knew I could make my project with it.

## Feedback on?  

Now that we know why Nuxt.js, it's time to dive into what I used in Nuxt.js. Keep in mind it's an opinionated list of some of the main stuff I used. Nuxt.js is much richer than just that.

<br/>

### Dynamic routing  

<br/>

Do you remember PHP? Yes I just said PHP, please do not be afraid. Nuxt.js has a routing system very similar to what PHP proposed: based on file names and directory structures.   
<br/>
Everything starts with the pages directory. Inside, you create your files which will be used as pages. By pages, I mean Vue.js components linked to a route in vue-router. But how to define these routes? Well you don't! When Nuxt.js builds your project, it looks inside your pages directory and generates it for you, based on the files name.  
<br/>
```js
pages/
--| index.vue
--| contact.vue
--| blog/
-----| index.vue
-----| _slug.vue
```
<br/>

What's happening here ?  

<br/>

First we have an index.vue file. This page will be displayed when navigating on the root of the app. You guessed it, the contact page will be displayed on the /contact path.  
<br/>
Next we have the subdirectory blog with an index file. This index page behaves the same as the previous one. Il will be displayed on the root but this time of the current directory : /blog.  
<br/>
Lastly, we have a _slug file. The _slug expression represents a dynamic parameter. It means, whenever I'll navigate to /blog/something, I'll display the _slug page in which I'll have access to a slug parameter which value will be (in this example) something.

<br/>

### Layout
<br/>

Layout allows you to easily configure the aspect of your app. It places itself one step higher than pages. In my case, I used it in a very simple way: to display components common to every page without repeating myself:

<br/>

```js
<Header />

<Nuxt />

<Footer />
```
<br/>

The `<Nuxt />` is replaced by the code of the page you're in, depending on your app and current route. It's only one use case of Nuxt.js layouts, you can easily find more use cases on the Nuxt.js documentation, such as creating a specific layout according to the resolution (mobile/tablet/desktop) for example.

<br/>

### Static mode
<br/>

One of my favorite feature so far! I knew my personal website - at least in a first version - did not need to request any APIs at runtime to display my content. So all my content could be generated at build time. But how could I take advantage of that? Well the Nuxt.js static mode does the exact job! It goes through all your pages and generates all your content, at build time. It also means I could use a static hosting services such as Netlify to host my site.  
<br/>
How to use the static mode? Update the nuxt.config.js file with the following property and that's it.  
<br/>
```js
target: 'static'
```

<br/>

### Nuxt content
<br/>

I wanted one specific feature : the ability to easily write and display blog posts. To do so, I tried one of the latest Nuxt.js module : @nuxt/content. 

To install this module, it is as easy as:

<br/>

```
npm install @nuxt/content
```
<br/>

and add the new module in nuxt.config.js:

<br/>

```js
{
   modules: [
      '@nuxt/content'
   ],
}
```
<br/>

At this point, the @nuxt/content module is installed. What's next? Creating your content. All you have to do is create files in a content directory. @nuxt/content supports all kinds of formats (markdown, json, csv, xml). I personally went with markdown as it is a format I'm comfortable with. Another thing to note is that, in addition to your content, you can add metadata to your content file. In my case, I added a title, a description and an image.

<br/>

Last step: how do I display the content I just created. First, you have to fetch it. For that, I used the asyncData method available on all pages of a Nuxt.js app. This method is called when navigating to the matching route and before initializing the component. In this method, you have access to a context object. By adding the @nuxt/content module, this context object is enriched with a $content property which will help us interact with our content. To fetch a content, it looks like this:

<br/>

```js
const article = await $content('articles', params.slug).fetch()

return { article }
```

<br/>

The parameters define the path of the content you're looking for. If no parameters are defined, it defaults to the root of the content directory. In my case, I created an articles subdirectory to organize my content. So I'm asking for the content inside a subdirectory called articles and named as the slug parameter in my current url.


<div class="article-image-container">
	<img src="/blog.png" />
</div>

## What I appreciated the most?

I appreciated a lot the simplicity of working with Nuxt.js. No time lost on complex configuration or importing a number of libraries. You just get a concise, easy-to-read and working architecture and configuration from the get-go, allowing you to work on your ideas and your content. This also works very well thanks to the clarity of the documentation and the great articles you can find on the Nuxt.js blog section. Big thumb up for that :)


## The biggest struggle I had?

The biggest struggle I faced on this project was about loading images. I decided to associate an image to every article I'll write. For the article you're currently reading, my first reflex was to add the image to the assets folder, like every other images of this site. But my image was never found. It turns out, the difference between this image and the other was that my image was loaded dynamically, according to the metadata of the article you're on.

<br/>

```js
<img :src="articleSummary.img" :alt="articleSummary.title" />
```

<br/>

Because of that, when Webpack bundles your app, it can not determine that this particular image is being used. Indeed, it never found an explicit use of it in your app at build time. So it removes it from your final bundle! I found a simple way to solve it  instead of placing my image in the assets folder, I put it in the static folder. The content in this folder is always part of your final bundle, without build time analysis. I hope this explanation will save you some struggle time if you meet the same issue.

## Conclusion

What to conclude? I learned a lot about Nuxt.js in this project and I loved what I discovered. Nuxt.js is really easy to get started with. It does not require a lot of experience, even with Vue.js and allows you to quickly focus on what matters: your ideas. This is something I'm looking for when working with a framework and Nuxt.js greatly succeeded with it. Also, for the use case of my projects, the amount of features I needed (static mode, @nuxt/content, etc) and quickly available effortlessly was impressive, so I'm glad I chose Nuxt.js.  
<br/>
I hope you learned some new stuff with this article and it gave you the desire to create your own personal website and to try out Nuxt.js!  
Please let me know your thoughts after this reading and in the meantime stay safe!
