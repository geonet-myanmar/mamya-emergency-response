# Ma Mya Dam Emergency Response Dashboard

A single-page situation dashboard for the Ma Mya Dam embankment failure in Myanaung Township, Ayeyarwady Region, Myanmar (situation as of 13 Oct 2026, 06:00).

**Live site:** https://geonet-myanmar.github.io/mamya-emergency-response/

## What it shows

- An interactive map of the Ma Mya creek flow path and the diversion canal, the 69 villages identified for relocation (in three priority tiers), the 0.5 / 1 / 2 / 4 km buffers, village tracts, schools, health facilities, bridges and roads
- Reservoir water levels for 10–13 Oct, against the full-supply (315 ft) and danger (326 ft) levels
- An elevation profile of the flow path (SRTM 30 m), with each village's depth below the reservoir surface
- Relocation and shelter figures by township, compared with the GIS exposure screen
- Exposure by distance band and village tract; schools, health facilities and road crossings near the flow path
- A news timeline (7–13 Oct 2026) that flags where reports disagree
- A searchable, sortable register of all 69 villages

## Data

| Source | Use |
|---|---|
| Official situation tables (12–13 Oct 2026) | Relocation, shelter and water-level figures. Decimals are truncated to integers; personal, organisation and department names are excluded. |
| Relocation KML (13 Oct 2026) | 69 villages with tiers, joined to MIMU village place codes |
| [MIMU GeoNode](https://geonode.themimu.info/) | Township and village-tract boundaries, villages, schools (2019), health facilities (2020), roads, bridges, reservoirs |
| [SRTM 30 m via OpenTopoData](https://www.opentopodata.org/datasets/srtm/) | Ground elevation at villages and along the stream |
| News reports (DVB, Eleven, MRTV, Ludu Nway Oo, Voice of Myanmar, Moemaka) | Timeline and reported dam facts; links are on the page |

The raw input files (scanned tables, maps, KML) are not included in this repository.

## Limits

The dashboard screens exposure by proximity and terrain. It is not a dam-break flood model and does not estimate inundation depth or arrival time.

## Deployment

The site is a static `index.html` served by GitHub Pages from the `main` branch root. Leaflet 1.9.4 loads from cdnjs and fonts from Google Fonts; all data is embedded in the page.
