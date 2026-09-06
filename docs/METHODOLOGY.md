# Methodology Notes — v0.7.0-alpha

## Synthetic geometry
Coral branches are represented as tapered 3D segments.

## Surface area
Each segment is approximated as a truncated cone:

```text
A = π (r1 + r2) s
s = sqrt(L² + (r1 − r2)²)
```

## Colony volume

```text
V = π L (r1² + r1 r2 + r2²) / 3
```

Current implementation sums branch volumes. Intersections are not subtracted.

## Df3D
Df3D is estimated using 3D box-counting over sampled points on the synthetic branch surface.

## Projected area
Projected area is estimated from XY-plane occupancy of sampled surface points.

## Height

```text
height = zmax − zmin
```

## Shelter volume

```text
shelter volume = projected area × colony height − colony volume
```

## Structural stress
The current conceptual stress control modifies distal-branch survival, branch length, branch radius, and number of child branches.
