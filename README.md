# infovis-assn2-supp
Supplementary material for SNU InfoVis assignment 2, 2025 Fall semester.

The file structure is explained below.
```
infovis-assn2-supp/
├─ assets/
│  ├─ datasets/
│  │  ├─ points/
│  │  ├─ lines/
│  ├─ world.geo.json
├─ tissot-implementation/
│  ├─ src/
│  │  ├─ ...
│  ├─ ...
├─ README.md
├─ report_template.zip
```
## Assets
`world.geo.json` contains a low-resolution world map which is quickly renderable in GeoJSON format. Refer to `tissot-implementation/src/components/MapDisplay.tsx` to see how to import and render this GeoJSON file.

Under `datasets/`, there are three *point* datasets and three *line* datasets. You can use these according to your task, or use your own datasets. Any additional information such as the geodesic length of lines should be calculated by yourself.

### Point datasets
1. GBIF - Architeuthis dux
2. GBIF - Tursiops aduncus
3. GBIF - Hydrochoerus hydrochaeris

### Line datasets
1. Flight Connections - Air India
2. Flight Connections - Air Astana
3. Flight Connections - United Airlines, 33% random sampling

Some datasets may be very large - you may sample or edit these datasets to fit your task. However, if you do so, state how you constructed your datasets clearly in your report, including which sampling method you used and how many points/lines (or the percentage) you sampled.

## tissot-implementation
`tissot-implementation/` is a sample React + TypeScript project which renders Tissot's indicatrices onto a world map with five distinct map projections: Mercator, Natural Earth, Orthographic, Equirectangular, and Azimuthal Equal-Area.

Use this project to investigate how to render and interact with geospatial data with `d3-geo`. If you are using TypeScript, you can also see how you can use predefined types for GeoJSON formats and `d3-geo` objects, which can be added to your project via `yarn add @types/d3`.

## Report Template
The report template can be found at `infovis-assn-supp/report_template.zip`. This template is identical to the report template for assignment 1.

## References and Tools
### Overview
- [Map Projections (Wiki)](https://en.wikipedia.org/wiki/Map_projection)
- [Tissot's indicatrices (Wiki)](https://en.wikipedia.org/wiki/Tissot%27s_indicatrix)
### Web Resources
- [d3](https://d3js.org)
- [d3-geo](https://d3js.org/d3-geo)
- [Observable D3 Gallery](https://observablehq.com/@d3/gallery)
### References
- Sarah E. Battersby and Fritz C. Kessler. Cues for interpreting distortion in map projections. *Journal of Geography,* 111(3):93-101, 2012.
- Paul Christopher Gosling and Elias Symeonakis. Automated map projection selection for gis. *Cartography and Geographic Information Science,* 47(3):261-276, 2020.
- Hyeon Jeon, Hyunwook Lee, Yun-Hsin Kuo, Taehyun Yang, Daniel Archambault, Sungahn Ko, Takanori Fujiwara, Kwan-Liu Ma, and Jinwook Seo. Unveiling high-dimensional backstage: A survey for reliable visual analytics with dimensionality reduction. In *Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems,* CHI '25, New York, NY, USA, 2025. Association for Computing Machinery.
- Kerkovits Krisztián. Comparing finite and infinitesimal map distortion measures. *International Journal of Cartography,* 5(1):3-22, 2019.
- Sylvain Lespinats and Michaël Aupetit. Checkviz: Sanity check and topological clues for linear and non-linear mappings. *Computer Graphics Forum,* 30(1):113-125, 2011.

