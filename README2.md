# 关于

## 网站

### In short

Very tiny static markdown website based on Docute. Docute is brilliant, I just gave it a little extra oomph by adding scripts to generate the ToC based on the contents (python3) and to assist in deployment on changes in the docs (bash). 

### Quick start

Clone the repo, edit the 2 lines in deployment/deployscript.sh and config.json simply by intuitively adding the info. More is possible when following docute.org's options guide.

### Markdown

The sourcePath you fill in in config.json will be the folder which will be checked for markdown files and folders. Only the folders in sourcePath will be checked, only .md files will be taken into account. Site will not bug out if other files are present. This means images can be included too. 

The table of contents will be created according to the file structure of sourcePath and the first line of the markdown files. Foldernames will be chapters, markdown titles will be one layer down, internal markdown headers will be another layer down.

### Submodules

While you could just make a folder to function as sourcePath and fill it with folders and markdown files, you could also include the folder as a submodule. In fact this is the intended way for collaboration. 

The benefit is you can share a docs repository containing only the folders and files with colleagues. They update there. A submodule update + deploy here updates the site with it's newest documentation.

### Images

This is all about navigating to the image file from the markdown file. There are three okay-ish ways to go here.

#### 1. Easiest when you don't have submodules.
Alternatively you could create an `images/` folder in the document root, next to sourcePath containing all images. Refer to images in this folder with `../../../images/yourimage.png`. Or even any file structure within there of course.

Problem with this approach is that when your sourcePath is a submodule, you won't have access to the documentroot.

#### 2. Right next to the markdown files
Just store the images in the same folder with it's respective markdown file.

#### 3. Create a folder in the markdown folder
This way you'll have the images stored separate, but still in close proximity to the related markdown files. Since image folder is inside the markdown folder it won't show up in the ToC.

```
## letsencrypt

```
sudo apt install certbot
sudo apt install python3-certbot-apache
sudo certbot run -a webroot -i apache -w /var/www/html -d example.com
```
