# middlemanSite

## middlemn init [project_name]
   - creates the project
   - source folder is where all the content lives

## middleman server  
   - takes all files, folders, and resources in our middleman project, compile them together, and serve them up on our local web server/host

## index.html.erb
   - the homepage for our entire website
   - erb stands for 'embedded ruby'
      - allows us to embed Ruby code inside our HTML and markdown files
      - we can create files without .erb extension, but won't be able to use Ruby code/logic in those files

## Frontmatter in Middleman
   - information we can store about the content pages on our site, like title, layout, author, language it's written in, etc.
   - for each page on the site, we can have different information about it, then we can access those variables and use them inside our middleman pages/layouts 
   - can be written in two languages
      1) YAML - a langugae used to define key-pair values
         - simple to use and not as syntax-heavy
         - we can access the title of the current page we're on, as stated below
         
         `<%= current_page.data.title %>`
      2) JSON - JavaScript Object notation
      - both of these are interchangable
   - we can access these frontmatter variables on any page that has embedded Ruby, then we can use <%= %> tags and access the information on those embedded Ruby pages
   - the best place to access them would be inside our templates/layouts 

## Helper Methods in Middleman
   - snippets of code you can add to your HTML/markdown file that simplify some common HTML tasks
      - for example, in a md file we don't want to include any ugly/messy HTML; when writing an HTML file, we may not want to go through the trouble of creating links, forms, etc

## Layouts in Middleman
   - special HTML files (high-level templates) that are used as templates for all the other HTML files on our websites
   - useful if we want all our sites to look the same, but on the content to look different 
   - layout.erb is the default layout that comes with middleman
      - it's an HTML skeleton and in the body we have a special `<%= yield %>` tag
         - this tag becomes the placeholder for all the code in the HTML file that we're currently browsing
      - we can create new layouts to be used with other HTML files but they need to be specified in front-matter using YAML
   - instead of manually specifying which layout to use in front-matter, there's a more powerful/efficient way of doing it through `config.rb`, in one place where all layouts are specified
   - we can also nest templates

## Partials in Middleman
   - special erb/html files where common elements are stored
      - for example, if we want the same header on mutliple layouts, this is where partials come in useful
   - naming convention
      - _partial.erb
      - the underscore in front of the file name is how middleman knows this is a partial