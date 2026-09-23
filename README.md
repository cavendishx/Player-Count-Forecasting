# 🎮 Player Count Forecasting

AI project focused on **Time Series Forecasting** of the number of active players in video games distributed on the Steam platform.

The goal is to predict the evolution of a game's **daily player count** over a **14-day forecasting horizon**, comparing different forecasting architectures.

## 🎯 Objective

The number of active players in a video game can vary significantly over time and is influenced by several factors, including:

* game updates;
* special events;
* promotions and price changes;
* review trends;
* temporal and seasonal patterns.

The project investigates the ability of different **deep learning forecasting models** to capture these dynamics and predict future player count.

## 🤖 Models Compared

Three forecasting models were compared:

### TCN — Temporal Convolutional Network

An architecture based on **Convolutional Neural Networks (CNNs)** designed for analyzing temporal sequences.

Temporal convolutions allow the model to analyze extended time windows and capture dependencies between observations that are distant in time.

### N-BEATSx

An extension of **N-BEATS** that integrates **exogenous variables** in addition to the main time series.

This allows the model to use additional information, such as price and review trends, when making predictions.

### N-HiTS

An evolution of N-BEATS that uses a **hierarchical, multi-resolution architecture** to analyze patterns at different temporal scales.

This approach allows the model to capture both short-term dynamics and patterns distributed across longer time intervals.

## 📊 Dataset

### Source

The data was collected from **SteamDB**:

[SteamDB](https://steamdb.info?utm_source=chatgpt.com)

### Coverage

The dataset includes approximately **350 Steam games**.

For each game, historical data was collected on:

* **daily/hourly player count**;
* number of **daily positive reviews**;
* number of **daily negative reviews**;
* **daily price** in euros;
* **markers**, representing special events often associated with positive or negative spikes in player activity.

The data is organized as time series for each game, making it possible to study both the temporal evolution of individual games and the ability of the models to generalize across different games.

## 🧪 Model Comparison

The three architectures are trained and evaluated on the same forecasting task, allowing their predictive capabilities to be compared.

The notebook contains the code required for:

* data preparation and preprocessing;
* time series construction;
* model training;
* forecast generation;
* performance evaluation;
* comparison of the obtained results.

## 📓 Notebook

The repository includes the notebook containing the complete implementation of the experiment and the results obtained.
