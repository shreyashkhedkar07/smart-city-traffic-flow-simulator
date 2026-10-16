# Smart City Traffic Flow Simulator

A beginner-friendly NumPy project that simulates hourly vehicle counts for 10 junctions over 30 days, identifies potential traffic bottlenecks, visualizes traffic patterns, and compares loop-based and vectorized calculations.

> **Note:** This project uses synthetic traffic data for educational purposes. It does not use live traffic feeds or measured data from a real city.

## Project objectives

- Simulate traffic for 30 days, 10 junctions, and 24 hours per day.
- Model morning and evening rush-hour patterns.
- Generate vehicle counts using NumPy's Poisson random distribution.
- Identify the busiest junctions and hours.
- Visualize traffic patterns with a heatmap and hourly traffic chart.
- Compare a nested-loop calculation with a vectorized NumPy operation.
- Export the generated data to CSV.

## Tools and libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Google Colab / Jupyter Notebook

These libraries are normally available in Google Colab.

## Run in Google Colab

1. Download `Smart_City_Traffic_Flow_Simulator.ipynb` from this project.
2. Open [Google Colab](https://colab.research.google.com/).
3. Select **File → Upload notebook**.
4. Upload the notebook.
5. Select **Runtime → Run all**.
6. Review the summary tables, charts, bottleneck candidates, and loop-versus-vectorized benchmark.

## Simulation dimensions

The traffic array has shape:

```python
(days, junctions, hours) = (30, 10, 24)
```

That represents **7,200 junction-hour records**.

## Main NumPy concepts practiced

- Array creation and shape inspection
- Random number generation with `np.random`
- Broadcasting
- Aggregation with `sum()` and `mean()`
- Peak detection with `argmax()`
- Array indexing and reshaping
- Vectorized operations and performance timing

## Outputs

- Average traffic heatmap by junction and hour
- Average traffic by hour of day
- Junction-wise traffic summary
- Top 10 junction-hour bottleneck candidates
- Loop-versus-vectorized runtime comparison
- `smart_city_traffic_data.csv` with one row per day, junction, and hour

The CSV contains columns for `Day`, `Junction`, `Hour`, and `Vehicle_Count`.

## How to interpret the results

Use the notebook's actual output to identify the busiest junction, busiest hour, and top bottleneck candidates. Results depend on the simulation's random seed and assumptions.

The benchmark speedup varies by runtime environment, so report the measured value from your own Colab run rather than assuming a fixed speedup.

## Limitations

- Traffic counts are synthetic, not live observations.
- The Poisson model is a simplified way to generate counts.
- Road capacity, traffic-light timing, vehicle speeds, accidents, and weather are not modeled.
- The weekend adjustment and rush-hour profile are illustrative assumptions.

## Resume description

Built a reproducible NumPy traffic simulator in Google Colab to generate 7,200 synthetic junction-hour records, identify peak traffic windows with aggregation and `argmax()`, visualize congestion candidates, and benchmark vectorized operations against Python loops.
