
## modify stuff

To modify something in the website, edit one of the `.qmd` file in this repo.

 * the basic document syntax is in [markdown](https://www.markdownguide.org/basic-syntax/)
 * more advanced website stuff are done with [quarto](https://quarto.org/docs/websites/)
 * if you want to add an image, you need to upload the image to the [assets/](assets/) [assets/gallery/](assets/gallery/) folder and link it in a page 


### multiple language support

You'll notice that to handle the 3 versions of the website (German, French, and English) text elements in the pages (in particular in `indez.qmd`) follow :

```
::: {.content-visible when-profile="en"}
Something in English.
:::

::: {.content-visible when-profile="fr"}
Quelque chose en français.
:::

::: {.content-visible when-profile="de"}
Etwas im Deutsch.
:::
```

Respect this structure anytime you want to add some text to anything. 

The most vexing thing is that images have to be put outside these blocks, but aside from that it shouldn't be not too much pain.

## render locally

Install [quarto](https://quarto.org/docs/get-started/), and then you can run the following command in the repo folder:

```sh
quarto render ; quarto render --profile de;quarto render --profile en; quarto render --profile fr
```

