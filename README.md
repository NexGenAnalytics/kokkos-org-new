# kokkos-org-new

# 1. Requirements 
- [Install Hugo](https://gohugo.io/installation/) version v0.111.3
- Need to be connected to internet to load [Paige theme](https://github.com/willfaught/paige) dependencies

<br />

# 2. How to work locally
- Install all requirements
- Clone [this repository](https://github.com/NexGenAnalytics/kokkos-org-new)
- Change directory: `<your-path-to-the-repository>`
- Edit source files (see below)
- To render the website, use: ``hugo server -D``
- Open Chrome, web server is available at http://localhost:`<assigned-port-depends>`
    - example: `http://localhost:1313`

<br />

# 3. How to add a blog post 
- Create a new .md file in the /content/blog/ folder
- There are 2 parts to display an article:
    - an information / header part and
    - a body part of the article
- Here is an example of a header for a new blog article:
    ```
    1 ---
    2 authors: ["author-name"]
    3 categories: ["categorie-1", "categorie-2", "categorie-3"]
    4 title: "your article title"
    5 date: "YYYY-MM-DD"
    6 description: "Your description here."
    7 ---
    ```
- From line 8 you can write all the text you want respecting the markdown rules of the [goldmark parser](https://github.com/yuin/goldmark)
- In addition, there are tags specific to the chosen theme. More information [here](https://github.com/willfaught/paige)

<br />

# 4. How to add a item in the top menu bar
- Go to `config.yaml`
- Add an item under the list below:
    ```
    6 languages:
    7  en:
    8   menu:
    9    main:
    ```
- It is necessary to specify 4 points: identifier, name, url and weight (location of the item in the top bar)
- Here is an example:
    - ```
      - identifier: "intern-name-to-identify-this-tab"
        name: "Name which is displayed"
        url: "/<path-to-folder>/<where-your-new-content-folder-is>/"
        weight: <number>
      ```
    - This tab will be before the items that have a weight lower than `<number>` and after the items that have a weight higher than `<number>`
- If you have no content at the `url`, you get an error. To solve it you have to create a page or a folder with the same name as your `identifier` (for more information see next section)

<br />

# 5. How to add a new page (not a blog)
- Create a new folder in the `content/` folder
- The name given will also be the identifier in the code and the name visible in the url 
- All folders in `content/` must have at least one file named `_index.md`
- This .md file must have a correct header (see part **3. How to add a blog post**)
- The content is then free following the markdown goldmark rules.

<br />

# 6. How to build static HTML files 
- Go to the root directory: `cd <your-path-to-the-repository>`
- Use the command line: `hugo`
- This command **generates the html code**, css, and more, to be able to deploy your website
- And puts it in an automatically created folder called **public/**

# Check the build 
You can check that the build is working well by running the build code with a small local python server. You must have python3 installed. This is not explained in this document.
- Change directory: `<your-path-to-the-repository>/public/`
- Execute the command: `python3 -m http.server`
- Web server is available at `http://localhost:8000` for example