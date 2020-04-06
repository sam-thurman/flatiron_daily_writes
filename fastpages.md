# Fastpages.ai

[Fastpages.ai](https://fastpages.fast.ai/) is a super handy tool for uploading jupyter labs as blog posts.  The fist cell in your Fastpage Jupyter Notebook must contain what's called 'front matter.' Front matter is metadata that as well as settings that turn on/off options in your notebook. For example setting `toc: true` will automatically generate a table of contents; setting `badges: true` will automatically include GitHub and Google Colab links to your notebook; setting `comments: true` will enable commenting on your blog post etc.</br>
An example of a front matter cell could look like...</br>
```
# Title
> Awesome summary

- toc:true- branch: master- badges: true- comments: true
- author: Hamel Husain & Jeremy Howard
- categories: [fastpages, jupyter]
```
</br>
Now you can start writing markdown cells and code cells one after the other to show your workflow.

[This](https://fastpages.fast.ai/jupyter/2020/02/20/test.html) tutorial contains good docuementation for writing blogs with Fastpages as well as some helpful tips and tricks to make your post shine.