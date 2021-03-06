The purpose of this file is to present a couple of basic plots using
`ggplot`.

First we create a dataframe containing variables for our plots.

    set.seed(1234)

    plot_df = tibble(
      x = rnorm(1000, sd = .5),
      y = 1 + 2 * x + rnorm(1000)
    )

First we show a histogram of the `x` variable.

    ggplot(plot_df, aes(x = x)) + geom_histogram()

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](template_files/figure-markdown_strict/x_hist-1.png)

Next we show a scatterplot of `y` vs `x`.

    ggplot(plot_df, aes(x = x, y = y)) + geom_point()

![](template_files/figure-markdown_strict/yx_scatter-1.png)
