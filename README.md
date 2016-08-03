# Jokestir.github.io

###Guide to configure github + jekyll to host personal website

0. Create a repository named username.github.io
1. Create a index.html file inside the repository inside. This is your homepage.
2. To style, create css/main.css.
3. Link index.html to main.css


Your website is ready.

### Configure Jekyll for using templates

0. Create a .gitignore file. And tell it to ignore the _site directory.
1. Create a _config.yml and tell jekyll the name of your project and the flavor of markdown to use.
2. Make a _layouts directory, and create file inside it called default.html. Move headers and footers from index.html into default.html
3. Update index.html to use default.html.
4. Create post.html in _layouts. It will contain liquid tags title,date,content. It will also use default.html.
5. Make _posts directory which will contain posts.YYYY-MM-DD-title-of-my-post.md. To list all the posts in one page...
6. Create blogs dir. Create index.html. And write for each loo. Commit. Go to username.github.io/blog
7. COnfigure so that there is blog dir in the url

**Done**.