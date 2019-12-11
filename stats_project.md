##### *Nate Wagner*

##### *Olivia Roberts*

##### *Dominic Ventura*

<br>

Introduction
------------

This project conducts statistical analysis on Uber and Lyft price
estimates, and seeks to find associations between price and other
variables. The data comes from
[Kaggle](https://www.kaggle.com/ravi72munde/uber-lyft-cab-prices), and
was collected via Uber and Lyft api queries and corresponding weather
conditions during a few weeks in November-December in 2018 by this
[user](https://github.com/ravi72munde). Inspiration for cleaning and
combining the rides and weather table came from
[here](https://www.kaggle.com/tangyx233/uber-lyft-cab-prices).

<br>

Exploratory Data Analysis
-------------------------

Our variable of interest is price, which ranges from $2.50 to $97.50.

<br>

<table>
<thead>
<tr>
<th style="text-align:left;">

-   Price
    </th>
    <th style="text-align:right;">

    -   Value
        </th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td style="text-align:left;">
        Min.
        </td>
        <td style="text-align:right;">
        2.50000
        </td>
        </tr>
        <tr>
        <td style="text-align:left;">
        1st Qu.
        </td>
        <td style="text-align:right;">
        9.50000
        </td>
        </tr>
        <tr>
        <td style="text-align:left;">
        Median
        </td>
        <td style="text-align:right;">
        16.00000
        </td>
        </tr>
        <tr>
        <td style="text-align:left;">
        Mean
        </td>
        <td style="text-align:right;">
        17.18493
        </td>
        </tr>
        <tr>
        <td style="text-align:left;">
        3rd Qu.
        </td>
        <td style="text-align:right;">
        24.00000
        </td>
        </tr>
        <tr>
        <td style="text-align:left;">
        Max.
        </td>
        <td style="text-align:right;">
        97.50000
        </td>
        </tr>
        </tbody>
        </table>

<br>

The distribution of price is about the same for both Uber and Lyft
![](stats_project_files/figure-markdown_github/unnamed-chunk-10-1.png)

#### How does price vary by cab type?

<br> Here is the min, max, median and mean price of a trip broken down
by the vehicle type

<br>
<table>
<thead>
<tr>
<th style="text-align:left;">

-   Uber Ride Type
    </th>
    <th style="text-align:right;">

    -   Uber Min Price
        </th>
        <th style="text-align:right;">

        -   Uber Max Price
            </th>
            <th style="text-align:right;">

            -   Uber Median Price
                </th>
                <th style="text-align:right;">

                -   Uber Mean Price
                    </th>
                    </tr>
                    </thead>
                    <tbody>
                    <tr>
                    <td style="text-align:left;">
                    Basic
                    </td>
                    <td style="text-align:right;">
                    6.0
                    </td>
                    <td style="text-align:right;">
                    44.0
                    </td>
                    <td style="text-align:right;">
                    9.5
                    </td>
                    <td style="text-align:right;">
                    9.764805
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    Lux
                    </td>
                    <td style="text-align:right;">
                    13.5
                    </td>
                    <td style="text-align:right;">
                    68.5
                    </td>
                    <td style="text-align:right;">
                    19.5
                    </td>
                    <td style="text-align:right;">
                    20.520902
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    LuxXL
                    </td>
                    <td style="text-align:right;">
                    23.0
                    </td>
                    <td style="text-align:right;">
                    89.5
                    </td>
                    <td style="text-align:right;">
                    28.5
                    </td>
                    <td style="text-align:right;">
                    30.286003
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    Shared
                    </td>
                    <td style="text-align:right;">
                    4.5
                    </td>
                    <td style="text-align:right;">
                    42.5
                    </td>
                    <td style="text-align:right;">
                    8.5
                    </td>
                    <td style="text-align:right;">
                    8.752105
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    XL
                    </td>
                    <td style="text-align:right;">
                    8.0
                    </td>
                    <td style="text-align:right;">
                    76.0
                    </td>
                    <td style="text-align:right;">
                    15.0
                    </td>
                    <td style="text-align:right;">
                    15.677541
                    </td>
                    </tr>
                    </tbody>
                    </table>

<table>
<thead>
<tr>
<th style="text-align:left;">

-   Lyft Ride Type
    </th>
    <th style="text-align:right;">

    -   Lyft Min Price
        </th>
        <th style="text-align:right;">

        -   Lyft Max Price
            </th>
            <th style="text-align:right;">

            -   Lyft Median Price
                </th>
                <th style="text-align:right;">

                -   Lyft Mean Price
                    </th>
                    </tr>
                    </thead>
                    <tbody>
                    <tr>
                    <td style="text-align:left;">
                    Basic
                    </td>
                    <td style="text-align:right;">
                    5.0
                    </td>
                    <td style="text-align:right;">
                    38.5
                    </td>
                    <td style="text-align:right;">
                    9.0
                    </td>
                    <td style="text-align:right;">
                    9.610261
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    Lux
                    </td>
                    <td style="text-align:right;">
                    10.5
                    </td>
                    <td style="text-align:right;">
                    75.0
                    </td>
                    <td style="text-align:right;">
                    19.5
                    </td>
                    <td style="text-align:right;">
                    20.414669
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    LuxXL
                    </td>
                    <td style="text-align:right;">
                    26.0
                    </td>
                    <td style="text-align:right;">
                    97.5
                    </td>
                    <td style="text-align:right;">
                    30.0
                    </td>
                    <td style="text-align:right;">
                    32.321568
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    Shared
                    </td>
                    <td style="text-align:right;">
                    2.5
                    </td>
                    <td style="text-align:right;">
                    22.5
                    </td>
                    <td style="text-align:right;">
                    7.0
                    </td>
                    <td style="text-align:right;">
                    6.029331
                    </td>
                    </tr>
                    <tr>
                    <td style="text-align:left;">
                    XL
                    </td>
                    <td style="text-align:right;">
                    9.0
                    </td>
                    <td style="text-align:right;">
                    65.0
                    </td>
                    <td style="text-align:right;">
                    13.5
                    </td>
                    <td style="text-align:right;">
                    15.308207
                    </td>
                    </tr>
                    </tbody>
                    </table>
                    <br>

There are 5 different vehicle types for Uber (Black, Black SUV, Uber
Pool, UberX, and UberXL) and there are 6 different vehicle types for
Lyft (Lux, Lux Black, Lux Black XL, Lyft, Lyft XL and Shared) So to make
proper comparisons, we made the following comparisons:

<br>

-   Lyft is comparable to UberX
-   Lux Black XL is comparable to Black SUV
-   Lyft XL is comparable to UberXL
-   Shared is comparable to Uber Pool
-   Black is comparable to Lux Black

<br>

We also combined Lux with Lux Black because they are essentially the
same vehicle type minus some small difference.

<br>

Here we can clearly see how the distribution of price changes depending
on the ride type.

<br>

![](stats_project_files/figure-markdown_github/unnamed-chunk-14-1.png)

#### Distance vs Price

<br> The distribution of price is roughly bimodal and a little skewed
right <br>
![](stats_project_files/figure-markdown_github/unnamed-chunk-15-1.png)

As we can see this by scatter plot, Lyft has a lower base price and also
a higher price ceiling. <br>
![](stats_project_files/figure-markdown_github/unnamed-chunk-16-1.png)

Here is a scatter plot of price vs distance broken down by ride type for
both Uber and Lyft. When broken down by ride type, it becomes clear
there is potentially some strong positive linear relationship between
price and distance. <br>
![](stats_project_files/figure-markdown_github/unnamed-chunk-18-1.png)![](stats_project_files/figure-markdown_github/unnamed-chunk-18-2.png)

<br>

<table class="table table-condensed">
<thead>
<tr>
<th style="text-align:left;">
Price.Vs.Distance
</th>
<th style="text-align:right;">
Lyft
</th>
<th style="text-align:right;">
LuxBlack
</th>
<th style="text-align:right;">
LuxBlackXL
</th>
<th style="text-align:right;">
Lux
</th>
<th style="text-align:right;">
LyftXL
</th>
<th style="text-align:right;">
Shared
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Lyft
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.7798634</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
Lux Black
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.8132575</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
Lux Black XL
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.6973414</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
Lux
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.8366301</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
Lyft XL
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.8144453</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
Shared
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.6420404</span>
</td>
</tr>
</tbody>
</table>
<table class="table table-condensed">
<thead>
<tr>
<th style="text-align:left;">
Price.Vs.Distance
</th>
<th style="text-align:right;">
Black
</th>
<th style="text-align:right;">
BlackSUV
</th>
<th style="text-align:right;">
UberPool
</th>
<th style="text-align:right;">
UberX
</th>
<th style="text-align:right;">
UberXL
</th>
<th style="text-align:right;">
WAV
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Black
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.7798634</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
Black SUV
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.8132575</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
UberPool
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.6973414</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
UberX
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.8366301</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
UberXL
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.8144453</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
</tr>
<tr>
<td style="text-align:left;">
WAV
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 50.00%">
</span>
</td>
<td style="text-align:right;">
<span
style="display: inline-block; direction: rtl; border-radius: 4px; padding-right: 2px; background-color: lightgreen; width: 100.00%">0.6420404</span>
</td>
</tr>
</tbody>
</table>

<br> To confirm, there are high correlations between distance and price
when broken down by ride type here. <br> <br>

#### Price on weekdays for Lyft

So far the comparisons have been on the base price between Uber and
Lyft. We only have data on surge prices for Lyft, but not Uber. So here
we make comparisons based off Lyft prices (including surge) for Lyft
only.

There doesn’t seem to be an effect of the day of the week on median
Surge Prices according to the data, and the weeks that it was collected.
This is obviously surprising, we would expect prices to be higher on
Fridays or even weekends.

<br>
![](stats_project_files/figure-markdown_github/unnamed-chunk-23-1.png)

<br>

#### Price on time of day

There also doesn’t seem to be much difference in the median of surge
price when it is broken down by the time of day, according to our data
and the weeks it was collected. <br>

![](stats_project_files/figure-markdown_github/unnamed-chunk-25-1.png)

#### Mean base price of an Uber trip

<br>

The estimated mean base price of an Uber trip in Boston:
*x̄* = 16

95% Confidence Interval:
(15.97, 16.03)

We are 95% confident that the true population mean base price of an Uber
Trip in Boston is between $15.97 and $16.03

Here we conduct a hypothesis test to see whether the mean base price of
an Uber trip in Boston differs from $10. The null and alternative
hypothesis are as follows:

*H*<sub>0</sub> : *μ* = 10

*H*<sub>*A*</sub> : *μ* ≠ 10

    ## 
    ##  One Sample t-test
    ## 
    ## data:  price$price
    ## t = 415.13, df = 274279, p-value < 2.2e-16
    ## alternative hypothesis: true mean is not equal to 10
    ## 95 percent confidence interval:
    ##  16.9668 17.0329
    ## sample estimates:
    ## mean of x 
    ##  16.99985

The conclusion is to reject the null hypothesis that the true population
mean of base price for Uber is equal to $10 at all alpha levels. The
p-value is essentially zero due to the large sample size and the effect
size of 0.75 confirms practical significance. The confidence interval
also agrees with our conclusion in that it does not contain $10.

<br> <br>

#### Proportion of Uber X trips

The estimated proportion of Uber X trips in Boston is
*p̂* = 0.39

95% Confidence Interval:
(0.384, 0.386)

We are 95% confident that the true population proportion of Uber X trips
in Boston is between 0.384 and 0.386

Here we conduct a hypothesis test to see whether the proportion of Uber
X trips in Boston is different from 0.30. The null and alternative
hypothesis are as follows:

*H*<sub>0</sub> : *p* = 0.30

*H*<sub>0</sub> : *p* ≠ 0.30

    ## 
    ##  1-sample proportions test with continuity correction
    ## 
    ## data:  as.integer(x) out of n, null probability 0.3
    ## X-squared = 13068, df = 1, p-value < 2.2e-16
    ## alternative hypothesis: true p is not equal to 0.3
    ## 95 percent confidence interval:
    ##  0.1984763 0.2014737
    ## sample estimates:
    ##         p 
    ## 0.1999708

The conclusion is to reject the null hypothesis that the true population
proportion of Uber X trips is equal to 0.30 at all alpha levels. The
p-value is essentially zero due to the large sample size and the effect
size of 0.18 says there is little practical significance. The confidence
interval also agrees with our conclusion in that it does not contain
0.30.

<br> <br>

#### Is the mean estimated price different between Uber and Lyft?

The null and alternative hypothesis are as follows

*H*<sub>0</sub> : *μ*<sub>*U*</sub> − *μ*<sub>*L*</sub> = 0

*H*<sub>*A*</sub> : *μ*<sub>*U*</sub> − *μ*<sub>*L*</sub> ≠ 0

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  mergeDF$price[mergeDF$cab_type == "Uber"] and mergeDF$price[mergeDF$cab_type == "Lyft"]
    ## t = -14.184, df = 580226, p-value < 2.2e-16
    ## alternative hypothesis: true difference in means is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.3994214 -0.3024348
    ## sample estimates:
    ## mean of x mean of y 
    ##  16.99985  17.35078

The conclusion is to reject the null hypothesis that the true population
difference in mean estimated price between Uber and Lyft is equal to 0
at all alpha levels. The p-value is essentially zero due to the large
sample size and the effect size of 0.11 says there may be little
practical significance. The confidence interval also agrees with our
conclusion in that it does not contain 0. Additionally, the mean
difference shows that Lyft has higher prices on average.

<br> <br> <br>

The first model just regresses price on cab type. <br> *Model 1*:
$$ \\begin{equation}
\\hat{Price}\_i = \\hat{\\beta}\_0 + \\hat{\\beta}\_1 Uber\_i
\\end{equation} $$

The second model controls for distance. <br> *Model 2*:
$$ \\begin{equation}
\\hat{Price}\_i = \\hat{\\beta}\_0 + \\hat{\\beta}\_1 Uber\_i +  \\hat{\\beta}\_1 Dist\_i
\\end{equation} $$

The Third model controls for distance and the ride type. <br> *Model 3*:
$$ \\begin{align\*}
\\hat{Price}\_i = \\hat{\\beta}\_0 + \\hat{\\beta}\_1 Uber\_i + \\hat{\\beta}\_2 Dist\_i  +\\sum\_{j=1}^{i}\\hat{\\beta\_3}\_j {Vehicle\_i}\_j  \\\\ 
\\end{align\*} $$

<table style="text-align:center">
<caption>
<strong>Regression Results</strong>
</caption>
<tr>
<td colspan="4" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td colspan="3">
<em>Dependent variable:</em>
</td>
</tr>
<tr>
<td>
</td>
<td colspan="3" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td colspan="3">
Price
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>

-   Model 1
    </td>
    <td>

    -   Model 2
        </td>
        <td>

        -   Model 3
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            \(1\)
            </td>
            <td>
            \(2\)
            </td>
            <td>
            \(3\)
            </td>
            </tr>
            <tr>
            <td colspan="4" style="border-bottom: 1px solid black">
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Uber
            </td>
            <td>
            -0.35
            </td>
            <td>
            -0.36
            </td>
            <td>
            0.24
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Distance
            </td>
            <td>
            </td>
            <td>
            2.97
            </td>
            <td>
            2.97
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Lux
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            10.80
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Lux XL
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            21.58
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Shared
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            -2.25
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            XL
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            5.81
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Constant
            </td>
            <td>
            17.35
            </td>
            <td>
            10.86
            </td>
            <td>
            3.07
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            <td>
            p = 0.00<sup>\*\*\*</sup>
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            </td>
            <td>
            </td>
            <td>
            </td>
            <td>
            </td>
            </tr>
            <tr>
            <td colspan="4" style="border-bottom: 1px solid black">
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Observations
            </td>
            <td>
            580,382
            </td>
            <td>
            580,382
            </td>
            <td>
            580,382
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            R<sup>2</sup>
            </td>
            <td>
            0.0003
            </td>
            <td>
            0.13
            </td>
            <td>
            0.87
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            Adjusted R<sup>2</sup>
            </td>
            <td>
            0.0003
            </td>
            <td>
            0.13
            </td>
            <td>
            0.87
            </td>
            </tr>
            <tr>
            <td colspan="4" style="border-bottom: 1px solid black">
            </td>
            </tr>
            <tr>
            <td style="text-align:left">
            <em>Note:</em>
            </td>
            <td colspan="3" style="text-align:right">
            <sup>*</sup>p\<0.1; <sup>**</sup>p\<0.05;
            <sup>***</sup>p\<0.01
            </td>
            </tr>
            </table>

<br>

To also confirm that Time of day as well as the day of the week has no
effect on surge prices we ran the following regression:

<br>

*Surge Price Model*:
$$ \\begin{align\*}
\\hat{Price}\_i = \\hat{\\beta}\_0 + \\hat{\\beta}\_1 Uber\_i + \\hat{\\beta}\_2 Dist\_i  +\\sum\_{j=1}^{i}\\hat{\\beta\_3}\_j {Vehicle\_i}\_j +\\sum\_{j=1}^{i}\\hat{\\beta\_4}\_j {TOD\_i}\_j +\\sum\_{j=1}^{i}\\hat{\\beta\_5}\_j {Weekday\_i}\_j\\\\  
\\end{align\*} $$

<table style="text-align:center">
<caption>
<strong>Regression Results</strong>
</caption>
<tr>
<td colspan="2" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
<em>Dependent variable:</em>
</td>
</tr>
<tr>
<td>
</td>
<td colspan="1" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
Price
</td>
</tr>
<tr>
<td colspan="2" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
Distance
</td>
<td>
3.67
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.00<sup>\*\*\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Lux
</td>
<td>
11.43
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.00<sup>\*\*\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Lux XL
</td>
<td>
24.04
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.00<sup>\*\*\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Shared
</td>
<td>
-4.15
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.00<sup>\*\*\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
XL
</td>
<td>
6.06
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.00<sup>\*\*\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Morning
</td>
<td>
0.01
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.78
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Night
</td>
<td>
-0.04
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.38
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Monday
</td>
<td>
0.02
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.69
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Saturday
</td>
<td>
0.01
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.87
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Sunday
</td>
<td>
0.01
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.80
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Thursday
</td>
<td>
0.001
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.99
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Tuesday
</td>
<td>
0.09
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.09<sup>\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Wednesday
</td>
<td>
0.08
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.18
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td style="text-align:left">
Constant
</td>
<td>
2.13
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
p = 0.00<sup>\*\*\*</sup>
</td>
</tr>
<tr>
<td style="text-align:left">
</td>
<td>
</td>
</tr>
<tr>
<td colspan="2" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
Observations
</td>
<td>
306,102
</td>
</tr>
<tr>
<td style="text-align:left">
R<sup>2</sup>
</td>
<td>
0.59
</td>
</tr>
<tr>
<td style="text-align:left">
Adjusted R<sup>2</sup>
</td>
<td>
0.59
</td>
</tr>
<tr>
<td colspan="2" style="border-bottom: 1px solid black">
</td>
</tr>
<tr>
<td style="text-align:left">
<em>Note:</em>
</td>
<td style="text-align:right">
<sup>*</sup>p\<0.1; <sup>**</sup>p\<0.05; <sup>***</sup>p\<0.01
</td>
</tr>
</table>

<br> <br>

<br>

#### Conclusion

The effect of Uber on the first model is -0.35, which is just the
difference in means of estimated price between Uber and Lyft. This
suggest that the base price of Uber is on average -$0.35 less than
Lyft’s base price. Adding distance to the second model doesn’t do much
to the coeffcient on Uber, but distance is statistically significant.
Now when we control for the vehicle type of the cab, that’s when we see
the difference in means switch signs, suggesting that controling for
distance and vehicle type, Uber is on average $0.24 more than Lyft’s
base price. When looking at the surge price model, we do confirm there
is no effect of the time of day and the day of the week on surge price
estimates in Boston, which is consistent with our boxplots above.

<br> <br> <br>
