# RealTimeFootballSpreadForecasting

## Overview
The goal of this project is to forecast the spread of American football games in real time using Gaussian Process Regression (GPR). 

This implementation scrapes the data from the play-by-play section of a selected game on ESPN.com and collects a new data point every time the possession changes, either through a score, a punt, a turnover, or turnover on downs. It then applies GPR to the collected data to forecast the spread for the remainder of the game. Rather than operating on the spread as a function of time, it instead considers the spread as a function of drives. Using the drives as the independent variable ensures that each data point is equally spaced and that the current momentum of the game can better propogate through to the forecast. 

## Gaussian Process Regression
This section provides a brief overview of Gaussian Process Regression. 

## Results
This section provides an example application. As a proud alumnus of the University of Central Florida (UCF), I wanted to test the code out on the UCF Knights 2021 season-opening win against the Boise State University (BSU) Broncos. The initial spread for this game was UCF -6.5. Figure 1 shows the game forecast based on this spread prior to the game starting, which includes the mean estimate, the credible intervals corresponding to +/- 3 standard deviations, and 50 random samples of the game forecast.

After a lengthy weather delay, BSU got off to a fast start, leading UCF by 14 points after the 1st quarter.

## Conclusions
