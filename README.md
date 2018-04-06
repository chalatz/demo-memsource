# Jekyll multilingual demo

This is a demo for a Jekyll multilingual site (english and japanese).

## Configurations

Various configurations can be applied through the `_data` folder (The Data section in forestry).

Current configurations are:

- **Settings:** Site-wide settings like title and email. Notice how the description supports two languages.
- **Menu:** The main menu is created from the data here. Made for two languages.
- **Langs-settings:** In here reside the available languages as well as their corresponding url segments. For instance, the short name for Japanese is jp, but its url segment is ja.
- **Speakers, Program:** Data that are used inside the Boston meetup page. In Two languages.

## Adding posts

Posts can be added from forestry's Posts section with the 'Add New' button. There are folders for the languages, but that's just for organizational purposes.

In the create/edit post page, you can fill the fields and write the text for the post's body. **Pay special attention to the 'lang' field**, as it defines the language of the post.

## Adding pages

Pages can be added from forestry's Pages section, with the 'Add New' button.

In the create/edit page page, you can fill the fields and write the text for the pages's body. **Pay special attention to the 'lang' field**, as it defines the language of the page.

Also, if you want the page to have more than one language variants, **you must fill the ref field in all the page's variations.**

All the page's variations **must have the same value in the ref field.**

Do not forget about the **permalink** link as well. Here you can for example set it to `/my-page/` for the english version, whereas you can set it to `/ja/my-page` for the japanese version. It goes without saying that these versions must have **the same value** for the `ref` field.

*In this demo the code for the pages is written in custom HTML. Markdown can be used as well, but the pages' template must be consistent and more plain. If more pages templates must be used, then their corresponding template files must be created.*

## Summing up

So the important things that make the site multiligual, are:

- The `Langs-settings` data file. Here the languages together with their url segments are set
- `lang` fields. Do not forget to set them for the pages and the posts.
- `ref` fields for the pages that need to have language variants.
- `permalink` fields for the pages.

## Markdown vs. HTML

Markdown was created for people to write blog posts fast. 

This suits tech people who like writing in code and markdown helps them focus on the content and not too much on the code itself.

Non tech people are benefited as well, while tools like forestry allows them to write content with a simple wysiwyg editor.

The editor for markdown is indeed simple. If you notice the forestry's text editor, it has no bells and whistles. 9 buttons and that's it. Just the basics.

Just paragraphs, lists, images etc. Plain HTML elements with no classes.

Markdown does not allow you to add classes in your content (well, actually Jekyll uses Kramdown, a variation of markdown, which allows you to add classes, but this might be difficult for non-tech people).

So if a post is written in markdown, it cannot consist of, say, two columns or its images to be floated right and left as needed. You will get single column content with images that take up the entire width of its row.

Posts and pages in Jekyll can have front matter fields, like the date or the author. Another good example is the hero image. You can define the image's path in a field and render it at the beginning of the post. Or you can have a boolean field to determine if a post will have comments or not.

So, markdown is used for writing the **body** of the post and the front matter fields to render content **before or after** the body. These fields can in fact be placed inside the body as well, but again, not suitable for non-tech people. HTML can also be used in markdown files (for example the code for an image with a class that floats the image), but that's a no-no for the non-techies.

So, if you want content to be edited by non-techies, markdown is the way to go, along with front matter fields. However this means that the posts and pages will have a consistent look.

If you want each of your pages to have a unique look, then custom HTML and CSS is the way to go. If the pages do not need frequent updating or they needn't be touched by non-techies, HTML is the best choice.

As for blog posts, markdown with front matter fields is the preferred way, and they will have a consistent look.

From my experience, if it can be afforded, HTML/CSS for pages, markdown for blog posts.
