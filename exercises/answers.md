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
2.      +proj=lcc +lat_1=59.8   +k_0=0.99998
3.      +proj=lcc +lat_1=59.437 +lat_2=60.171
4.      +proj=lcc +lat_1=59.8   +lat_0=59.8   +lon_0=24.8
5.      +proj=lcc +lat_1=59.8   +lat_0=59.8   +lon_0=24.8  +x_0=1000000 +y_0=1000000
```

## Projections.3: Tranverse Mercator

```
1.      +proj=tmerc
2.      +proj=tmerc +k_0=0.9996 +lon_0=27 +x_0=500000
3a.     1 cm
3b.     250 km
3c.     100 km
3d.      10 km
3e.     500  m
3f.       2  m
3g.       5 um
```

## Ellipsoids:

```
1.      +R=1
2.      +ellps=intl
3.      +a=6378388.0 +rf=297.0
4.      +a=6378206.4 +b=6356583.8
