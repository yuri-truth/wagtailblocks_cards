Wagtail Blocks: Cards
=====================

This Wagtail block can be used to add a series of cards. It is styled on the editor screen.

![Screenshot](screenshot.png)

Installation
------------

Run:

    pip install wagtailblocks-cards

Then add `wagtailblocks_cards` to your installed apps.

Usage
-----

Include the block wherever relevant and add it to any StreamField.

    from wagtailblocks_cards.blocks import CardsBlock

Then:

    body = StreamField([
      ('cards', CardsBlock())
    ])

Finally, template the block as usual.

Fields
------

Use the following names when templating:

* image - ImageChooserBlock
* title - CharBlock
* text - TextBlock
* link - PageChooserBlock

Notes
-----

You can also add a CardsBlock inside of a StructBlock or other structual block types for more control. You may want to inject more custom CSS to make it span the full width if you aren't using help text, or change the number of columns.

If [wagtailfontawesome](https://github.com/alexgleason/wagtailfontawesome) is installed, this app will detect it and use [fa-clone](http://fontawesome.io/icon/clone/) by default.
