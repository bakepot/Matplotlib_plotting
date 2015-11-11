# Matplotlib_plotting

### figure_plotting.py
The functions in this script are used by other Python scripts to plot various data.

Usage:
```
import figure_plotting as figplt

d1 = np.linspace(0., 2.*np.pi, num=600)
d2 = np.cos(2.*np.pi*1*d1)
xlabel = r'$\omega={:4.1f}$'.format(14.3)
figplt.basicplot([d1,  d2],
          {'color': 'b', 'linestyle': 'dashed', 'label': 'data'},
          xlabel=xlabel)
```

### Matplotlib style sheet
The style sheet is saved in a location similar to this: /usr/local/bin/anaconda/lib/python2.7/site-packages/matplotlib/mpl-data/stylelib/

Use `plt.style.use('bakerplotstyle')` to use the style sheet.  Python interpreter must be restarted to reload a modified style sheet.
