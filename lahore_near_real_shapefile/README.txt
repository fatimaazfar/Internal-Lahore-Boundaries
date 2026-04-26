Lahore near-real locality layer

Files:
- lahore_locality_voronoi.shp : approximate locality polygons for Lahore District
- lahore_locality_points.shp : source locality points used to build polygons
- lahore_district_boundary.shp : Lahore District boundary used for clipping
- matching GeoJSON exports are included

How it was built:
1. Lahore District boundary extracted from PakData/GISData (GADM-derived district polygon).
2. Dense locality point list for Lahore parsed from Paintmaps' "Neighborhoods and Villages of Lahore" coordinate list.
3. Voronoi polygons generated from locality points in projected CRS and clipped to Lahore District.

Important limitations:
- This is NOT an official neighborhood boundary layer.
- These polygons are influence zones around named localities, not legal/administrative UC or town borders.
- It is much better than sparse nearest-anchor labeling, but still approximate.
- Best use: dashboard labeling, proximity-based area assignment, exploratory mapping.
- Not recommended for legal planning, cadastral work, or formal reporting.

Suggested usage:
- For point labeling, do point-in-polygon against lahore_locality_voronoi.
- Keep lahore_locality_points visible at low zoom for sanity-checking.
- For critical zones like Walled City, Shahdara, Ichra, Garhi Shahu, Mughalpura, etc., manually refine a few polygons after visual review.
