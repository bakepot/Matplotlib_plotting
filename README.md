# Matplotlib_plotting
This script aids plotting of data in a style that I like and fits most of the data I deal with.  It is used as a module that can be imported into another Python file, with the plotting functions called with a single line (versus the typical several lines).

### TO-DO
* add subplotting function
* add ability to plot y-data vs various x-data arrays (right now, y-data can only be plotted vs the first and only x-data array, necessitating an interpolation function for other datasets with different x-data spacing)
* add contour plot feature
* add ability to override linestyle and linewidth with arguments to the calling function

### figure_plotting.py
The functions in this script are used by other Python scripts to plot various data.

Usage:
```
import figure_plotting as figplt

freq = 3.  # [Hz], frequency
t = np.linspace(0., 2.*np.pi, num=600)
d1 = np.sin(2.*np.pi*freq*t)
d2 = np.cos(2.*np.pi*freq*t)
title = r'Sinusoid with $\omega={:4.1f}$ rad/s'.format(freq*2.*np.pi)
dataset1 = (t, (d1, d2))
param1 = ({'label': '$\\theta_1$', 'color': 'b'},
          {'label': '$\\dot{\\theta_1}$', 'color': 'k'})
figplt.basicplot(dataset1, param1, xlabel=r'time, [s]',
                 ylabel=r'magnitude', title=title,
                 suptitle='Angles vs Time', filename='Angles_vs_Time.png', xmax=np.max(t))
```

### Matplotlib style sheet
The style sheet is saved in a location similar to this: /usr/local/bin/anaconda/lib/python2.7/site-packages/matplotlib/mpl-data/stylelib/

Use `plt.style.use('bakerplotstyle')` to use the style sheet.  Python interpreter must be restarted to reload a modified style sheet.

### Notes and References
