# Create your Jupyter Book template

This page covers how to create a Jupyter Book with your own content.
You've got three primary ways to create your Jupyter Book.

## by starting with a minimal book

Running the following command will create a new Jupyter Book with a few
content pages and a Table of Contents to get you started:

```bash
jupyter-book create mybookname
```

This will create a new book using your content in `mybookname/`. You'll then need to

1. Add your content to `mybookname/content/`
2. Modify `mybookname/_data/toc.yml` to match your content
3. Modify `mybookname/_config.yml` to the configuration you'd like

Note that if you choose to create the book template and later add content
to it, you can quickly **generate a basic Table of Contents** by running
the following command:

```bash
jupyter-book toc mybookname/
```

## by modifying the Demo Book

If you'd like to see a more fully-functioning demo book for inspiration, you can
create the book that lives at the [jupyter-book website](https://jupyterbook.org)
by adding the `--demo` flag:

```bash
jupyter-book create mybookname --demo
```

See the previous section for a description of all of the relevant files you
should modify for your book.


## by using a pre-existing book configuration

If you've used Jupyter Book before, you can quickly generate a *new* book using a pre-existing
set of folders and files. These are all available as arguments in the command line interface.

For example, if you have your book's content in a folder structure like this:

```bash
myoldbook/
├── content
│   ├── root_test.md
│   └── tests
├── _data
│   └── toc.yml
├── images
│   └── tests
├── mylicense.md
├── myextrafolder
│   └── myextrafile.txt
└── config.yml
```

You can generate a Jupyter Book from it with the following command:


```bash
jupyter-book create mybookname --content-folder myoldbook/content \
                               --toc myoldbook/_data/toc.yml \
                               --config myoldbook/_config.yml \
                               --license myoldbook/mylicense.md \
                               --extra-files myoldbook/myextrafolder
```

This will create a new Jupyter Book using these files. In this case, you need to ensure
that the values in `_config.yml` are correct, and that the Table of Contents (`toc.yml`) file
has the structure that you want.

## Next step: convert your book content into HTML

Now that you've got a Jupyter Book folder structure, we can create
the HTML for each of your book's pages. That's covered in the next
section.