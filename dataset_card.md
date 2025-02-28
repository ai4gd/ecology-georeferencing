# Dataset Card: Georeferencing Figures in Ecology Papers

This document describes a dataset intended to benchmark LLM-based georeferencing of maps, i.e. the ability to look at a map and correctly determine its physical location on Earth. The dataset consists of 114 ecology research papers in PDF format, each of which contains at least one figure that includes a map. For each paper, the dataset provides the (manually-determined) georeferenced location of that map (in geojson format).

## Dataset Overview

**Dataset Snapshot:**

| Characteristic | Value |
|---|---|
| Size of Dataset | 1.5 GB |
| Number of Instances | 114 |
| Number of Fields | 1 |
| Labeled Classes | 1 |
| Number of Labels | 114 |
| Average Labels Per Instance | 1 |
| Algorithmic Labels | 0 |
| Human Labels | 114 |
| Other Characteristics | n/a |

**Content Description:**

The dataset consists of 114 ecology research papers in PDF format, each of which contains at least one figure that includes a map. For each paper, the dataset provides the (manually-determined) georeferenced location of that map (in geojson format). Each underlying paper remains subject to its original copyright.

## Motivations & Intentions

**Motivations:**

This dataset is intended to benchmark LLM-based georeferencing of maps, i.e., the ability to look at a map and correctly determine its physical location on Earth.

**Suitable Use Cases:**

Evaluate LLM capabilities around georeferencing, tune prompts for georeferencing.

**Research and Problem Spaces:**

This dataset is intended to benchmark LLM-based georeferencing of maps, i.e., the ability to look at a map and correctly determine its physical location on Earth.

## Access

**Access:**

* **Access Type:** External - Open Access
* **Documentation Link(s):** https://github.com/google-research/ecology-georeferencing 
* **Policy Link(s):** LICENSE file in the repo (specifies Apache 2.0 license) for code

## Provenance

**Collection:**

* **Methodology Detail(s):** Source: Manually reviewed several repositories of open-access ecology literature for papers with suitable licenses and suitable figures, then manually created georeferencing information
* **Source Description(s):** See index.csv and license_overview.csv

## Example of Data Points

**Primary Data Modality:**

Geospatial Data

**Typical Data Point:**

```json
{
  "type": "FeatureCollection",
  "name": "status_assessment_of_the_endangered_1",
  "crs": {
    "type": "name",
    "properties": {
      "name": "urn:ogc:def:crs:OGC:1.3:CRS84"
    }
  },
  "features": [
    {
      "type": "Feature",
      "properties": {
        "id": null
      },
      "geometry": {
        "type": "MultiPolygon",
        "coordinates": [
          [
            [
              [
                71.070661025837012,
                38.768814100057
              ],
              [
                71.070661025837012,
                40.497599161469005
              ],
              [
                74.407392714631172,
                40.497599161469005
              ],
              [
                74.407392714631172,
                38.768814100057
              ],
              [
                71.070661025837012,
                38.768814100057
              ]
            ]
          ]
        ]
      }
    }
  ]
}
