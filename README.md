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
