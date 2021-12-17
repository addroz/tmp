
First data: https://zenodo.org/record/3574566#.YaSWFdDMKUk

Second data: https://github.com/wri/global-power-plant-database/blob/master/README.md

for i in range(21):
    sys.stdout.write('\r')
    # the exact output you're looking for:
    sys.stdout.write("[%-20s] %d%%" % ('='*i, 5*i))
    sys.stdout.flush()
    sleep(0.25)
