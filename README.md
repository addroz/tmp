
First data: https://zenodo.org/record/3574566#.YaSWFdDMKUk

Second data: https://github.com/wri/global-power-plant-database/blob/master/README.md

Third data: https://data.open-power-system-data.org/conventional_power_plants/

for i in range(21):
    sys.stdout.write('\r')
    # the exact output you're looking for:
    sys.stdout.write("[%-20s] %d%%" % ('='*i, 5*i))
    sys.stdout.flush()
    sleep(0.25)

n=21, replace range(21) with range(n), then add j = (i + 1) / n inside the loop, and replace the write statement with this slight modification: sys.stdout.write("[%-20s] %d%%" % ('='*int(20*j), 100*j))
