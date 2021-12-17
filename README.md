
First data: https://zenodo.org/record/3574566#.YaSWFdDMKUk

Second data: https://github.com/wri/global-power-plant-database/blob/master/README.md

import progressbar
from time import sleep
bar = progressbar.ProgressBar(maxval=20, \
    widgets=[progressbar.Bar('=', '[', ']'), ' ', progressbar.Percentage()])
bar.start()
for i in xrange(20):
    bar.update(i+1)
    sleep(0.1)
bar.finish()
