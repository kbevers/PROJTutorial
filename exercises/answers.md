# Answers to the PROJ tutorial exercises

## Projections.1: UTM

```
1.      +proj=utm +zone=35
2.      +proj=utm +zone=60 +south
3.      +proj=utm +zone=35 +ellps=intl


## Projections2.: LCC

1.      +proj=lcc +lat_1=59.8
2.      +proj=lcc +lat_1=59.437 +lat_2=60.171
3.      +proj=lcc +lat_1=59.437 +lat_2=60.171 +k_0=1.00002
4.     +proj=lcc +lat_2=59.437 +lat_1=60.171 +k_0=1.00002 +lon_0=24.8 +lat_0=59.8
5.      +proj=lcc +lat_2=59.437 +lat_1=60.171 +k_0=1.00002 +lon_0=24.8 +lat_0=59.8 +x_0=1000000 +y_0=1000000
 ```