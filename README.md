# Climate Change: Heat and Wave-height by North and South Hemispheres
## Authors:
Sean Nakagomi, instructed by Dr. Galen Egan

## Requirements:
This project was created using Python via Google Colab.

## Introduction:
Global warming is a very serious situation that I have heard about for a good amount of my life. But despite hearing about this issue for so long, I really don't know how hot it has been getting over the years, nor do I know how to determine that value. This project aims to give me those answers, while comparing the North and South Hemispheres.

We will identify and isolate the long-term warming trend through sea surface temperature (SST) and forecast it just shy of four decades into the future.

For the additional step portion, we will also look at wave heights for each hemisphere to determine which side has the biggest waves.

## Data:
We will use data queried from the ERA5 Reanalysis Product. A reanalysis is a dataset that combines historical observations (which we trust within the uncertainty of the instrument used to make the measurement, but cannot feasibly cover the entire world) with a physics-based computer model of the earth system (which is not generally as accurate as a measurement, but can at least cover the entire world) to produce consistent global datasets of all variables we are interested in. ERA5 is produced by the European Center for Medium-Range Weather Forecasting (ECMWF), widely regarded as the best forecasting center in the world. Therefore, it is the preferred data product for studying how the Earth's climate has evolved over the past century.

## Data analysis: Sean_Nakagomi_Climate_Analysis.ipynb
We first grouped the data by hemispheres (north and south), split the data into test-train sets, and identified and isolated the long-term warming trend through SST, by generating a Power Spectral Density as well as creating graphs of the two hemispheres using a 2-year window moving average (median and mean) on the train data. We then quickly Googled the dates associated with the local minimums and maximums to spot any trends such as various active hurricane and typhoon seasons which were annotated in the notebook.

Next, we forecast these trends just shy of four decades into the future using the Prophet Model and calculated each of their mean absolute errors (MAE) to gauge accuracy.

For the additional step, we again split the oceans into the two hemispheres like before, but focused on wave-height, and we looked at both the mean and five-number summary for the two hemispheres, comparing them to each other.

We then dove deeper and created a tidy dataframe that included wave-height data for both hemispheres at each date where all included oceans had recorded data and compared the two hemispheres via a histogram and a box plot filtered monthly.

Lastly, we described the findings obtained in the analysis.

## Licence:
MIT License

Copyright (c) 2024 Sean Nakagomi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
