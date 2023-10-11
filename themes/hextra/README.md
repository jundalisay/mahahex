      {{- if (.Site.Params.navbar.displayTitle | default true) }}
        <span class="mx-2 font-extrabold inline select-none" title="{{ .Site.Title }}">{{- .Site.Title -}}</span>
      {{- end }}

      
    <article class="w-full break-words flex min-h-[calc(100vh-var(--navbar-height))] min-w-0 justify-center pb-8 pr-[calc(env(safe-area-inset-right)-1.5rem)]">
      <main class="w-full min-w-0 max-w-6xl px-6 pt-4 md:px-12">
        <h1 class="text-center mt-2 text-4xl font-bold tracking-tight text-slate-900 dark:text-slate-100">{{ .Title }}</h1>
        <div class="content">
          {{ .Content }}
        </div>
      </main>
    </article>

node 17.1.0


{{ define "main" }}
  <div class='mx-auto flex {{ partial "utils/page-width" . }}'>
    {{ partial "sidebar.html" (dict "context" .) }}
    {{ partial "toc.html" . }}
    <article class="w-full break-words flex min-h-[calc(100vh-var(--navbar-height))] min-w-0 justify-center pb-8 pr-[calc(env(safe-area-inset-right)-1.5rem)]">
      <main class="w-full min-w-0 max-w-6xl px-6 pt-4 md:px-12">
        <div class="content">
          <h1>{{ .Title }}</h1>
          {{ .Content }}
        </div>
        <div class="mt-16"></div>
        {{ partial "components/last-updated.html" . }}
        {{ partial "components/comments.html" . }}
      </main>
    </article>
  </div>
{{ end }}




<div class="squote grid grid-cols-4 gap-2" data-sal="slide-right">
  <div class="col-span-2">
    {{ .Inner | safeHTML }}
  </div>
  <div style="border-radius: 999px; height: 50px; width: 50px; background-size: cover; background-repeat: no-repeat;" class="{{ $a }} col-span-2" ></div>  
</div>



<div class="squote grid grid-cols-4 gap-2" data-sal="slide-right">
  <div class="col-span-2">
    {{ .Inner | safeHTML }}
  </div>
  <div style="border-radius: 999px; height: 50px; width: 50px; background-size: cover; background-repeat: no-repeat;" class="{{ $a }} col-span-2" ></div>  
</div>


            <h3><a style="color: inherit; text-decoration: none;" class="block font-semibold mt-8 text-2xl " href="{{ .RelPermalink }}">{{ .Title }}</a></h3>
            <p class="opacity-80 mt-6 leading-7">
              {{- partial "utils/page-description" . }}
              <span class="inline-block"> <a class="text-[color:hsl(var(--primary-hue),100%,50%)] underline underline-offset-2 decoration-from-font" href="{{ .RelPermalink }}">Read more →</a> </span>
            </p>

            
<section class="bg-white dark:bg-gray-900">
    <div class="py-8 px-4 mx-auto max-w-screen-xl text-center dark:bg-gray-900 lg:py-16 lg:px-12">
        <a href="#" class="inline-flex justify-between items-center py-1 px-1 pr-4 mb-7 text-sm text-gray-700 bg-gray-100 rounded-full dark:bg-gray-800 dark:text-white hover:bg-gray-200 dark:hover:bg-gray-700" role="alert">
            <span class="text-xs bg-primary-600 rounded-full text-white px-4 py-1.5 mr-3">New</span> <span class="text-sm font-medium">Flowbite is out! See what's new</span> 
            <svg class="ml-2 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd"></path></svg>
        </a>
        <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-6xl dark:text-white">We invest in the world’s potential</h1>
        <p class="mb-8 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 xl:px-48 dark:text-gray-400">Here at Flowbite we focus on markets where technology, innovation, and capital can unlock long-term value and drive economic growth.</p>
        <div class="flex flex-col mb-8 lg:mb-16 space-y-4 sm:flex-row sm:justify-center sm:space-y-0 sm:space-x-4">
            <a href="#" class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-white rounded-lg bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 dark:focus:ring-primary-900">
                Learn more
                <svg class="ml-2 -mr-1 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
            </a>
            <a href="#" class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-gray-900 rounded-lg border border-gray-300 hover:bg-gray-100 focus:ring-4 focus:ring-gray-100 dark:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:focus:ring-gray-800">
                <svg class="mr-2 -ml-1 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2 6a2 2 0 012-2h6a2 2 0 012 2v8a2 2 0 01-2 2H4a2 2 0 01-2-2V6zM14.553 7.106A1 1 0 0014 8v4a1 1 0 00.553.894l2 1A1 1 0 0018 13V7a1 1 0 00-1.447-.894l-2 1z"></path></svg>
                Watch video
            </a>  
        </div>
        <div class="px-4 mx-auto text-center md:max-w-screen-md lg:max-w-screen-lg lg:px-36">
            <span class="font-semibold text-gray-400 uppercase">FEATURED IN</span>
            <div class="flex flex-wrap justify-center items-center mt-8 text-gray-500 sm:justify-between">
                <a href="#" class="mr-5 mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">                  
                </a>
                <a href="#" class="mr-5 mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
                    sadfasdf                     
                </a>
                <a href="#" class="mr-5 mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
sdf
                </a>         
            </div>
        </div> 
    </div>
</section>




<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/5097752/263550533-c18343ca-3848-4230-b5c0-ee989d7916da.png">
  <img alt="Hextra" src="https://user-images.githubusercontent.com/5097752/263550528-663599f9-17a1-4686-b5c4-3da233b5034d.png">
</picture>

<div align="right">
<a href="https://github.com/imfing/hextra/actions/workflows/pages.yml"><img alt="GitHub Actions Status" src="https://github.com/imfing/hextra/actions/workflows/pages.yml/badge.svg"></a> <a href="https://app.netlify.com/sites/hugo-hextra/deploys"><img alt="Netlify Status" src="https://api.netlify.com/api/v1/badges/61d6e55a-2447-487e-b59f-c9537e5df175/deploy-status"></a>
</div>

## Features


- **Beautiful Design** - Inspired by Nextra, Hextra utilizes Tailwind CSS to offer a modern design that makes your site look outstanding.
- **Responsive Layout and Dark Mode** - It looks great on all devices, from mobile, tablet to desktop. Dark mode is also supported to accomodate various lighting conditions.
- **Fast and Lightweight** - Powered by Hugo, a lightning-fast static-site generator housed in a single binary file, Hextra keeps its footprint minimal. No Javascript or Node.js are needed to use it.
- **Full-text Search** - Built-in offline full-text search powered by FlexSearch, no additional configuration required.
- **Battery-included** - Markdown, syntax highlighting, LaTeX math formulae, diagrams and Shortcodes elements to enhance your content. Table of contents, breadcumbs, pagination, sidebar navigation and more are all automatically generated.
- **Multi-language and SEO Ready** - Multi-language sites made easy with Hugo's multilingual mode. Out-of-the-box support is included for SEO tags, Open Graph, and Twitter Cards.

## Quick Start

### Use the template

Using the [Hextra Starter Template](https://github.com/imfing/hextra-starter-template) is the simplest method to bootstrap a new website with Hextra theme. Get started by clicking the "Use this template" button on the template repository page.

The template repository also includes a [GitHub Actions workflow](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow) for deploying your website to GitHub Pages.

<img alt="Hextra Starter Template" src="https://user-images.githubusercontent.com/5097752/263551418-c403b9a9-a76c-47a6-8466-513d772ef0b7.jpg" width=600/>

### Usage

Refer to the [documentation](https://imfing.github.io/hextra/docs) for more information.

## Contributing

Contributions are welcome!
Check out the [contributing guide](.github/CONTRIBUTING.md) to get started.

## License

[MIT License](./LICENSE)
