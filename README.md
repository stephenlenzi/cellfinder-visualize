# Cellfinder-visualize User Guide

## About

`cellfinder-visualize` is a tool for post-cellfinder data visualisation and analysis.
The core aims are to provide:

 - Publication quality visualisations of cellfinder experiments for multiple samples
 - Standardised publication quality plots of cell counts for different region sets
   - Easy toggling of regions of interest
   - Matching visualisations to quantifications
   - Lateralised views
   - Slice views
 - Statistical analysis  (in progress)


`cellfinder-visualize` is a tool developed by [Stephen Lenzi](https://github.com/stephenlenzi) in the [Margrie Lab](https://www.sainsburywellcome.org/web/groups/margrie-lab), generously supported by the [Sainsbury Wellcome Centre](https://www.sainsburywellcome.org/web/).

<img src='https://user-images.githubusercontent.com/12136220/183618125-b1e60c25-0695-4040-979c-4b3afd3024c4.png' width="550">

## Installation


```conda create -n  cellfinder-visualize python```

```conda activate  cellfinder-visualize```

```git clone https://github.com/SainsburyWellcomeCentre/cellfinder-visualize.git```

```cd cellfinder-visualize```

```pip install -e .```

## Usage

Simply run from the commandline as follows

```conda activate  cellfinder-visualize```

```cellfinder_visualize```

This will open a GUI for selecting parameters

<img src='https://user-images.githubusercontent.com/12136220/179235778-3520e509-01da-46d0-8711-bf5bad588193.png' width="1000">


```experiment dir``` should be a directory containing cellfinder output directories

```output dir``` should be a directory for saving any outputs for your sample

```coronal slice start``` if you want to show only a coronal subsection this value is the start in microns

```coronal slice end``` if you want to show only a coronal subsection this value is the end of that section in microns

```root``` if checked the whole brain outline will be shown

```show reference structures``` if checked, several brain regions will be added for reference only

```filter cells by structure``` if checked, cells displayed will be restricted to the regions listed in ```region list```

```hemisphere``` whether to display and count cells in left/right/both hemispheres

```slice root``` if checked, and a subregion is selected (e.g. only one hemisphere, or a coronal section) then all other unselected regions will not be visible

```subsample factor``` show every nth cell of the number chosen

```highlight subregion``` outlines will be drawn for subregions that contain the string in this box. i.e. if you wanted to highlight layer 5 in displayed regions, then ```5``` would achieve this.

```region list``` each item in this list will be displayed and included in any analysis

```colors``` color labels that each correspond to items in the region list.

```reference region``` the region used to normalise cell counts to.

```brainrender``` if checked, brainrender will run.

```barplots``` if checked, barplots will be generated of the cell counts.

```load additional obj files``` if any .obj files are present in the directory given then they will be rendered in the brainrender view.



The end result should be bar plots per sample indicating the counts and percentages of cells in each region:

<img src='https://user-images.githubusercontent.com/12136220/190441882-f79dfdc7-24d2-4bdf-a469-ba9fa8d573e6.png' width="550">

<img src='https://user-images.githubusercontent.com/12136220/190442296-2a3d9969-81cb-469f-8d26-f43d5251678d.png' width="550">



And also a pooled plot indicating the averages for all samples and the individual points:


<img src='https://user-images.githubusercontent.com/12136220/190442598-a752da25-01c3-4df1-a592-66350995751d.png' width="550">


Together with a brainrender of the samples and target regions:

<img src='https://user-images.githubusercontent.com/12136220/178687766-f50dccf7-57ab-4fa2-b75a-d9534479f930.png' width="400">

<img src='https://user-images.githubusercontent.com/12136220/178718223-57daac92-5453-4680-9a22-ef93bc121430.png' width="400">

<img src='https://user-images.githubusercontent.com/12136220/178718515-05c63fa5-a3ec-4579-9dfb-35b18aab8a09.png' width="400">

Any .obj files in the directory hierarchy will be automatically displayed e.g.:

<img src='https://user-images.githubusercontent.com/12136220/178738417-a8cf975d-5437-425f-8527-e1bab7c21725.png' width="400">
