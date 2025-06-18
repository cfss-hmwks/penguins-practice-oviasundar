<!-- prettydoc::html_pretty: -->
<!--       theme: cayman -->
<!--       highlight: github -->

## R Markdown

Here we are going to learn a bit about penguins!

## Penguins

See below for averages on penguins.

    ## # A tibble: 344 × 8
    ##    species island    bill_length_mm bill_depth_mm flipper_length_mm body_mass_g
    ##    <fct>   <fct>              <dbl>         <dbl>             <int>       <int>
    ##  1 Adelie  Torgersen           39.1          18.7               181        3750
    ##  2 Adelie  Torgersen           39.5          17.4               186        3800
    ##  3 Adelie  Torgersen           40.3          18                 195        3250
    ##  4 Adelie  Torgersen           NA            NA                  NA          NA
    ##  5 Adelie  Torgersen           36.7          19.3               193        3450
    ##  6 Adelie  Torgersen           39.3          20.6               190        3650
    ##  7 Adelie  Torgersen           38.9          17.8               181        3625
    ##  8 Adelie  Torgersen           39.2          19.6               195        4675
    ##  9 Adelie  Torgersen           34.1          18.1               193        3475
    ## 10 Adelie  Torgersen           42            20.2               190        4250
    ## # ℹ 334 more rows
    ## # ℹ 2 more variables: sex <fct>, year <int>

    ## # A tibble: 3 × 3
    ##   sex    avg_bill avg_mass
    ##   <fct>     <dbl>    <dbl>
    ## 1 female     37.3    3369.
    ## 2 male       40.4    4043.
    ## 3 <NA>       37.8    3540

## Your work

Summarize the dataset in a meaningful way (use AT LEAST two of the key
functions from slide \#12)

    penguins %>%
      filter(species == "Adelie") %>%
      group_by(flipper_length_mm) %>%
      summarize(bill_length_mm = mean(bill_length_mm, na.rm = TRUE))

    ## # A tibble: 33 × 2
    ##    flipper_length_mm bill_length_mm
    ##                <int>          <dbl>
    ##  1               172           37.9
    ##  2               174           37.8
    ##  3               176           40.2
    ##  4               178           36.6
    ##  5               179           37.5
    ##  6               180           39.4
    ##  7               181           38.0
    ##  8               182           39.6
    ##  9               183           39.2
    ## 10               184           37.9
    ## # ℹ 23 more rows

    data("women")

    women

    ##    height weight
    ## 1      58    115
    ## 2      59    117
    ## 3      60    120
    ## 4      61    123
    ## 5      62    126
    ## 6      63    129
    ## 7      64    132
    ## 8      65    135
    ## 9      66    139
    ## 10     67    142
    ## 11     68    146
    ## 12     69    150
    ## 13     70    154
    ## 14     71    159
    ## 15     72    164
