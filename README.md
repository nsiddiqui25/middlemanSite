# middlemanSite

middlemn init [project_name]
   - creates the project
   - source folder is where all the content lives

middleman server  
   - takes all files, folders, and resources in our middleman project, compile them together, and serve them up on our local web server/host

index.html.erb
   - the homepage for our entire website
   - erb stands for 'embedded ruby'
      - allows us to embed Ruby code inside our HTML and markdown files
      - we can create files with erb extension, but won't be able to use Ruby code/logic in those files

Frontmatter in Middleman
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