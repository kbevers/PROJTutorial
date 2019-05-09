# Answers to the PROJ tutorial exercises

## Projections.1: UTM

```
1.      +proj=utm +zone=35
2.      +proj=utm +zone=60 +south
3.      +proj=utm +zone=35 +ellps=intl
```


## Projections2.: LCC

```
1.      +proj=lcc +lat_1=59.8
2.      +proj=lcc +lat_1=59.437 +lat_2=60.171
3.      +proj=lcc +lat_1=59.437 +lat_2=60.171 +k_0=1.00002
4.     +proj=lcc +lat_2=59.437 +lat_1=60.171 +k_0=1.00002 +lon_0=24.8 +lat_0=59.8
5.      +proj=lcc +lat_2=59.437 +lat_1=60.171 +k_0=1.00002 +lon_0=24.8 +lat_0=59.8 +x_0=1000000 +y_0=1000000
```

## Geodesics

```
Helsinki,  UTM:  6672241.54   385592.95
Tallinn,   UTM:  6590881.40   372106.37
Mid point, UTM:  6631561.47   378849.66
Mid point, GEO:  59.804039062602   24.840482644156

Meditations:
1.      Probably not
2.      geod +lat_1=60.171 +lon_1=24.938 +lat_2=59.437 +lon_2=24.745 +n_S=2 +ellps=GRS80 -f "%.12f"
3.      Avoids a bit of truncation of the azimuth, and *may* use a slightly superior algorithm (check the code!)
4.      Start with the PROJ stuff...
```
