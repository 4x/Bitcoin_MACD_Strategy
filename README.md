Bitcoin - Basic MACD Trading Strategy
================

Go long when the MACD crosses above the signal line, close out the position when it crosses back under. Vice versa for short positions (optional).

Example - Default MACD settings, Long only
==========================================

From a risk return perspective, this simple strategy seems to outperform buy and hodl in the long run.

``` r
source("config/Config.R")
btc.close <- FetchBTCInfo(param           = "market-price",   
                          data.identifier = "btc.close", 
                          date.start      = "2012-01-01")
names(btc.close) <- "close"

btc.results <- SimpleMACDStrategyUnivariate(asset         = btc.close, 
                                            asset.name    = "BTC CHART",
                                            nFast         = 12,
                                            nSlow         = 26,
                                            nSig          = 9,
                                            long.only     = TRUE,
                                            plot.strategy = TRUE,
                                            plot.results  = TRUE,
                                            strategy.name = "MACD Strategy")
```

![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-1.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-2.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-3.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-4.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-5.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-6.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-7.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-8.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-9.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-10.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-11.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-12.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-13.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-14.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-15.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-16.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-17.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-18.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-19.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-20.png)![](README_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-21.png)

Donations
---------

If you find this software useful and/or you would like to see additional extensions, feel free to donate some crypto:

-   BTC: 1QHtZLZ15Cmj4FPr5h5exDjYciBDhh7mzA
-   LTC: LhKf6MQ7LY1k8YMaAq9z3APz8kVyFX3L2M
-   ETH: 0x8E44D7C96896f2e0Cd5a6CC1A2e6a3716B85B479
-   DASH: Xvicgp3ga3sczHtLqt3ekt7fQ62G9KaKNB

Or preferably, donate some of my favorite coins :)

-   GAME: GMxcsDAaHCBkLnN42Fs9Dy1fpDiLNxSKX1
-   WAVES: 3PQ8KFdw2nWxQATsXQj8NJvSa1VhBcKePaf

Licensing
---------

Copyright 2017 Essential Data Science Consulting ltd. ([EssentialQuant.com](http://essentialquant.com "EssentialQuant") / <jellenvermeir@essentialquant.com>). This software is copyrighted under the MIT license: View added [LICENSE](./LICENSE) file.
