The Visual Hierarchy
================
Your Name

In this lesson, we will illustrate different methods of visualizing
information. The purpose of this exercise is to determine which methods
are the most effective – in terms of ‘ease of interpretation.’ You will
rank a number of different visualizations – of the same data – in terms
of how easily you can draw comparisons. This will lead to prescriptive
suggestions about constructing visualizations, which will be useful when
designing graphics.

## Define figures for different tasks

See code in `master.Rmd`….

### Plot all visual tasks figures

The following six figures all show identical data – they each depict a
dataset detailing attributes about different models of car. Each
observation in the dataset is a single model of vehicle; the attributes
depicted below are the Drive style (Forward Wheel Drive (`fwd`) and Rear
Wheel Drive (`rwd`)) and Body style (`hatchback`, `sedan`, or `wagon`).
Each figure depicts the number of cars that fall into each category; for
instance, the number of cars in the dataset that are both `fwd` and
`hatchback`.

**Complete the following tasks:**

1.  For each visualization, describe *how information is visually
    encoded.* Is information shown via shape, position, color, size, or
    something else?
2.  Answer the question “Which is larger: The count of `wagons` with
    `fwd` Drive OR the count of `wagons` with `rwd` Drive? By how much
    is one larger than the other?”
3.  Rank the following visualizations *in terms of how well they help
    you answer question (2) above.* Rate the most helpful visualization
    as 1, and the least helpful as 6; do not allow ties between
    visualizations.

<!-- end list -->

``` r
df_figs %>% pull(fig)
```

    ## [[1]]

![](challenge_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

    ## 
    ## [[2]]

![](challenge_files/figure-gfm/unnamed-chunk-10-2.png)<!-- -->

    ## 
    ## [[3]]

![](challenge_files/figure-gfm/unnamed-chunk-10-3.png)<!-- -->

    ## 
    ## [[4]]

![](challenge_files/figure-gfm/unnamed-chunk-10-4.png)<!-- -->

    ## 
    ## [[5]]

![](challenge_files/figure-gfm/unnamed-chunk-10-5.png)<!-- -->

    ## 
    ## [[6]]

![](challenge_files/figure-gfm/unnamed-chunk-10-6.png)<!-- -->
