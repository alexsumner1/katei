# 家庭 (Katei)

This is a Ruby-based static site generator thrown together in a couple of hours. It makes use of [Redcarpet](https://github.com/vmg/redcarpet) to convert Markdown to HTML.

It's pretty badly written, but if you're just wanting something to turn a tree structure full of markdown into some kind of webpage, this may not be a bad option!

## Usage
1. Simply create a template called `template.html` in the root directory, build it up and throw the template marker "`{{content}}`" somewhere in it. 
2. Create two folders, one called `content` and one called `output`. Like the names imply, content is where your Markdown will live, and output is where the HTML will be thrown, ready to be chucked on a webserver or an S3 bucket somewhere. 
3. Add some files and create a folder structure inside the `content` directory. For example, an `index.md`, perhaps a `blog` folder, etc. The folder structure you create in markdown will be reflected in the HTML output. 
4. Any files starting with a number, for example `20220101-test.md` will be compiled into a blog-style, newest first, x-per-page format, accessible via paged files in that directory, and still individually accessible too for permalinking. 
5. Run `./katei`, and let it spit everything out into the `output` folder. 
6. Have fun!
