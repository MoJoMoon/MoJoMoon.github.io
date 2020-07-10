---
layout: post
title:      "Color Guide to Seaborn Palettes"
date:       2020-07-10 09:25:34 +0000
permalink:  color_guide_to_seaborn_palettes
---


Seaborn arguably has one of the most rich visualization packages for python. It contains beautiful colors with powerful controls of parameters for a wide array of plots. While exploratory data analysis is one of the most important steps in the machine learning pipeline, interpretation and sharing of data can be considered an even more vital component of data science. In data visualization color is necessarily involved, and colors have an influence on their observer. In this guide we will display the full range of color palettes offered by Seaborn to give anyone intending to visualize data a comprehensive perspective of their options.
To begin, Seaborn has 170 different palette options. The entire list can be accessed easily after importing seaborn:
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
In order to create a plot, you need data, so we will read in our dataset with pandas:
df = pd.read_csv(‘advertising.csv’)
Then create a plot with seaborn, here we set hue to the age_group column. Now use any single number or letter as a string value for palette:
sns.pairplot(df, hue=’age_group’, palette=’d’)
This will create an error message that looks like this:
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
~\Anaconda3\lib\site-packages\seaborn\palettes.py in color_palette(palette, n_colors, desat)
    231                 # Perhaps a named matplotlib colormap?
--> 232                 palette = mpl_palette(palette, n_colors)
    233             except ValueError:

~\Anaconda3\lib\site-packages\seaborn\palettes.py in mpl_palette(name, n_colors)
    455     else:
--> 456         cmap = mpl.cm.get_cmap(name)
    457         if cmap is None:

~\Anaconda3\lib\site-packages\matplotlib\cm.py in get_cmap(name, lut)
    182             "Colormap %s is not recognized. Possible values are: %s"
--> 183             % (name, ', '.join(sorted(cmap_d))))
    184
The error message that is returned will also have a complete list of all the palette values that you can choose from. The list is here
[‘Accent’, ‘Accent_r’, ‘Blues’, ‘Blues_r’, ‘BrBG’, ‘BrBG_r’, ‘BuGn’, ‘BuGn_r’, ‘BuPu’, ‘BuPu_r’, 
 ‘CMRmap’, ‘CMRmap_r’, ‘Dark2’, ‘Dark2_r’, ‘GnBu’, ‘GnBu_r’, ‘Greens’, ‘Greens_r’, ‘Greys’, ‘Greys_r’, ‘OrRd’, 
 ‘OrRd_r’, ‘Oranges’, ‘Oranges_r’, ‘PRGn’, ‘PRGn_r’, ‘Paired’, ‘Paired_r’, ‘Pastel1’, 
 ‘Pastel1_r’, ‘Pastel2’, ‘Pastel2_r’, ‘PiYG’, ‘PiYG_r’, ‘PuBu’, ‘PuBuGn’, ‘PuBuGn_r’, 
 ‘PuBu_r’, ‘PuOr’, ‘PuOr_r’, ‘PuRd’, ‘PuRd_r’, ‘Purples’, ‘Purples_r’, ‘RdBu’, ‘RdBu_r’, 
 ‘RdGy’, ‘RdGy_r’, ‘RdPu’, ‘RdPu_r’, ‘RdYlBu’, ‘RdYlBu_r’, ‘RdYlGn’, ‘RdYlGn_r’, ‘Reds’, 
 ‘Reds_r’, ‘Set1’, ‘Set1_r’, ‘Set2’, ‘Set2_r’, ‘Set3’, ‘Set3_r’, ‘Spectral’, ‘Spectral_r’, 
 ‘Wistia’, ‘Wistia_r’, ‘YlGn’, ‘YlGnBu’, ‘YlGnBu_r’, ‘YlGn_r’, ‘YlOrBr’, ‘YlOrBr_r’, ‘YlOrRd’, 
 ‘YlOrRd_r’, ‘afmhot’, ‘afmhot_r’, ‘autumn’, ‘autumn_r’, ‘binary’, ‘binary_r’, ‘bone’, 
 ‘bone_r’, ‘brg’, ‘brg_r’, ‘bwr’, ‘bwr_r’, ‘cividis’, ‘cividis_r’, ‘cool’, ‘cool_r’, ‘coolwarm’, ‘coolwarm_r’, ‘copper’, ‘copper_r’,
 ‘cubehelix’, ‘cubehelix_r’, ‘flag’, ‘flag_r’, ‘gist_earth’, ‘gist_earth_r’, ‘gist_gray’, ‘gist_gray_r’, ‘gist_heat’, ‘gist_heat_r’, ‘gist_ncar’, ‘gist_ncar_r’,
 ‘gist_rainbow’, ‘gist_rainbow_r’, ‘gist_stern’, ‘gist_stern_r’, ‘gist_yarg’, 
 ‘gist_yarg_r’, ‘gnuplot’, ‘gnuplot2’, ‘gnuplot2_r’, ‘gnuplot_r’, ‘gray’, ‘gray_r’,
 ‘hot’, ‘hot_r’, ‘hsv’, ‘hsv_r’, ‘icefire’, ‘icefire_r’, ‘inferno’, 
 ‘inferno_r’, ‘magma’, ‘magma_r’, ‘mako’, ‘mako_r’, 
 ‘nipy_spectral’, ‘nipy_spectral_r’, ‘ocean’, ‘ocean_r’, ‘pink’, ‘pink_r’,
 ‘plasma’, ‘plasma_r’, ‘prism’, ‘prism_r’, ‘rainbow’, ‘rainbow_r’,
 ‘rocket’, ‘rocket_r’, ‘seismic’, ‘seismic_r’, ‘spring’, ‘spring_r’,
 ‘summer’, ‘summer_r’, ‘tab10’, ‘tab10_r’, ‘tab20’, ‘tab20_r’, ‘tab20b’,
 ‘tab20b_r’, ‘tab20c’, ‘tab20c_r’, ‘terrain’, ‘terrain_r’, ‘twilight’,
 ‘twilight_r’, ‘twilight_shifted’, ‘twilight_shifted_r’, ‘viridis’, ‘viridis_r’, ‘vlag’, ‘vlag_r’, ‘winter’, ‘winter_r’]
The rest of this post will display each of these palettes in a pairplot to demonstrate these colorways in scatterplot and kde plot varieties. You can browse through for a colorway that suites your needs, or use finder and select a name from the list above. There are truly several beautiful options in this library. Enjoy.

These are the colorways made available to you through Seaborn. Of this selection, there is surely a palette which will enrich your visualization, and help convey the story that your data has to express. Thanks for reading.
