# Testing plotlyhtml converter

This repo contains two HTML versions of a simple notebook converted. One uses the plain `nbconvert` html converter, the other one uses [plotlyhtml](https://github.com/plotly/plotlyhtmlexporter):

```bash
jupyter nbconvert --to html --output converted-with-plainhtml.html plotly-html-test.ipynb
jupyter nbconvert --to plotlyhtml --output converted-with-plotlyhtml.html plotly-html-test.ipynb
```

I'm looking into an issue with `plotlyhtmlexporter`, this repo is to test/illustrate the issue so the devs can conveniently see it.

In the version converted with the plotly converter, I'm seeing two issues:

1. The first cell, that ends with the code `cf.set_config_file(offline=True, world_readable=True, theme='ggplot')`, displays (in the HTML file) a massive amount of text corresponding to the JavaScript output.

1. The actual plot is *not* displayed in the second cell.

