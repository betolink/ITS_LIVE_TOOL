# ITS_LIVE_TOOL

```{note}
add figures, images of processed data, data access gifs etc. to readme 
```

# About

`ITS_LIVE_TOOL` is a package designed to aid users working with the
[Inter-mission Time Series of Land Ice Velocity and Elevation](link)
(ITS_LIVE) dataset. The package provides functions for accessing data as
well as various methods to process ITS_LIVE observations. 

# Installation 

Eventually, we hope to have a pip install. For now, install via:

`pip install pip+https://github.com/vdevauxchupin/ITS_LIVE_TOOL`

# Overview
 
## Data Access + Organization

We implement 3 object classes to store ITS_LIVE velocity data and auxiliary information with the goal of making it efficient and intuitive to keep track of and scale your analysis of ITS_LIVE data. 

The illustration below provides a high-level overview of the main object classes in `ITS_LIVE_TOOL`

```{note}still need to decide on final figure for this?
```
[illustration will go here ? ]()


### Interactive Widget

This is an interactive map widget designed to streamline access to ITS_LIVE image pair velocity datasets and creation of `ITS_LIVE_TOOL` objects. To see an example of the interactive widget, check out `interactive.ipynb`. Use the widget in your workflow by importing the `interactive` module.

### `Glacier`, `Glacier_Centerline`, `Glacier_Point` objects
```{note}
once we have rendered docs, link add hyper links for these objects
```

These are meant to be container objects to store related pieces of data in easier-to-use locations. Depending on your purposes, create `Glacier`, `Glacier_Centerline` or `Glacier_Point` objects. You can do this using the interactive map widget or by manulaly passing input arguments. See `obj_setup.ipynb` for examples of each. `Glacier` objects contain RGI V7 outlines stored as `geopandas.GeoDataFrame` objects. `Glacier_Centerlines` contain OGGM centerlines, also stored as `geopandas.GeoDataFrame` objects. `Glacier_Point` objects use scripts made available by the developers of the ITS_LIVE dataset to access ITS_LIVE image pair ice velocity data. 

## Data Processing

```{note}
link to book not working, still working on best way to build book 
```

We demonstrate and make available two processing routines. Be sure to
check out the accompanying [book]() and consider if either of these are
appropriate for your data and use case. Note that these methods are in
active development and thus should be considered in *beta* phase. Please
perform your own data inspection and due diligence if implementing these
methods.

### Data filtering 

Pre-processing methods for inspecting and removing outliers from ITS_LIVE time series. Temporal baseline threshold methods focus specifically on cases where movement of slower glaciers may be near or below the noise threshold of the imaging sensors and feature tracking algorithms. These methods aim to determine a minimum temporal baseline threshold appropriate for a given dataset. 

### Gaussian Process
**to add** description 

### Inversion

**to add** Description – link to full description and examples

## How to use

For a detailed, code-based walk through of ITS_LIVE_TOOL functionality, check out `roadmap.ipynb` notebook. This will demonstrate how to access ITS_LIVE data and use the interactive map widget and container objects provided in this package. It will also briefly describe and show sample outputs from the processing methods implemented in this package. For in-depth explanations of the processing methods, check out the individual notebooks where those steps will be described in much more detail.

## Citing 
- not sure if its appropriate/necessary here but i see some packages have a readme section for how to cite them if someone uses their work

## Contact

- add our emails

## Acknowledgements
- co-authors, funding sources, other collaborators, anythign else?

## References

### Data
- cite ITS_LIVE, RGI v7 outlines, OGGM centerlines
### Methods 
- cite gaussian process, temporal inversion literature here?
### Software
- packages used

## Contributing
maybe add something like: We welcome community contributions to this work! Please don't hesitate to raise an issue, start a discussion our reach out to us over email