# *coastTrain*: a global reference library for coastal ecosystems

#### Description
This global dataset is a point-record training set  of  occurrences (n=193,105) of 7 coastal ecosystem types (tidal flat, mangrove, photic coral reef, saltmarsh/tidal marsh, seagrass, rocky intertidal, kelp forest), terrestrial other and permanent water. The dataset integrates occurrence records from four data sources:

- [Global Tidal Flats](http://intertidal.app)
- [Global Tidal Wetlands Change](https://globalintertidalchange.org)
- [Global Mangrove Watch](https://www.globalmangrovewatch.org/)
- [Allen Coral Atlas](https://allencoralatlas.org/). 

Data is given in the geojson format with 15 field attributes for each data point:
1.	Type – the geospatial feature type, typically a feature
2.	ID – unique identifier for each individual record
3.	Lat- latitudinal coordinates
4.	Lon – longitudinal coordinates
5.	Class – categorical variable of an integer representing an ecosystem type of the record following the coastTrain classification scheme.
6.	Method – principal method of data acquisition in the primary source project
7.	Scale – reference scale and indicator of appropriate spatial scale for use
8.	IUCN_Realm – Realm is one of five major components of the bio-sphere as described in the IUCN Global Ecosystem Typology
9.	IUCN_Biome – Biome is a component of a realm united by broad features of ecosystem structure and one or a few major ecological drivers as described in the IUCN Global Ecosystem Typology 
10.	IUCN_Funct – Functional group is a group of related ecosystems within a biome that share common ecological drivers, as described in the IUCN Global Ecosystem
11.	IUCN_FunGC– The IUCN Ecosystem Typology Ecosystem Functional Group Code
12.	RefDatSta – the beginning of the time period for which the occurrence record has either been confirmed against reference imagery or as indicated as applicable by the source project.
13.	RefDatEnd – the end of the time period for which the occurrence record has either been confirmed against reference imagery or as indicated as applicable by the source project.
14.	Proj_Ref – a code to reference the source mapping project that submitted the data.
15.     Ecosys_Typ - coastal ecosystem types


#### Citation
Use of any aspect of this training requires full attribution (see CC-BY licence). Please cite the published paper:

>Murray, N. J., Bunting, P., Canto, R., Hilarides, L., Kennedy, E. V., Lucas, R., Lyons, M. B., Navarro, A., Roelfsema, C. M., Rosenqvist, A., Spalding, M., Toor, M. & Worthington, T. A. (in submission) coastTrain: a global reference library for coastal ecosystems. Remote Sensing.

*coastTrain: a global reference library for coastal ecosystems* 
![img](figs/coastTrain.JPG)

#### Licence
This software is licensed under a Creative Commons Attribution-Non Commercial 4.0 International License. [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

#### Maintainer: 
Nicholas Murray (nicholas.murray@jcu.edu.au).

#### Usage notes
*coastTrain* is intended to be quickly incorporated into classification models applied to earth observation data. Obtain the latest versioned release of coastTrain in [GeoJSON](https://geojson.org/) format archived on Zenodo at doi: [xxx].

*coastTrain* is a set of point occurrences representing the coastal ecosystem types in the table below. The occurrence records were developed primarily by satellite image interpretation with additional reference to published studies, coastal atlases and any existing dataset. Every point in coastTrain was checked against time-stamped satellite imagery acquired during our reference period for 2014-2016. Each point is appended with an integer value to act as a numeric record for use in classification models. Class definitions broadly follow those developed by the [IUCN Global Ecosystem Typology](https://global-ecosystems.org/). Please see the published paper for further information.

| Ecosystem type                     | Class Value | IUCN Realm                    | IUCN Biome          | IUCN Code | IUCN Ecosystem Functional Group  (link)                                   |
| ---------------------------------- | :----:| :---------------------------- | :------------- | :-:   | :-------------------------------------------------------------------------------------- | 
| Terrestrial other (non-intertidal) |   `0` | N/A                           | N/A            | N/A   | N/A                                                                                     | 
| Permanent water                    |   `1` | N/A                           | N/A            | N/A   | N/A                                                                                     | 
| Tidal flat                         |   `2` | Marine-Terrestrial            | Shorelines     | MT1.2 | [Muddy Shorelines](https://global-ecosystems.org/explore/groups/MT1.2)                  |
| Mangroves                          |   `3` | Marine-Freshwater-Terrestrial | Brackish tidal | MFT1.2| [Intertidal forests and shrublands](https://global-ecosystems.org/explore/groups/MFT1.2)|
| Coral reef                         |   `4` | Marine                        | Marine shelf   | M1.3  | [Photic coral reefs](https://global-ecosystems.org/explore/groups/M1.3)                 |
| Saltmarsh / tidal marsh            |   `5` | Marine-Freshwater-Terrestrial | Brackish tidal | MFT1.3| [Coastal saltmarshes and reedbeds](https://global-ecosystems.org/explore/groups/MFT1.3) |
| Seagrass                           |   `6` | Marine                        | Marine shelf   | M1.1  | [Seagrass meadows](https://global-ecosystems.org/explore/groups/M1.1)                   |
| Rocky intertidal                   |   `9` | Marine-Terrestrial            | Shorelines     | MT1.1 | [Rocky Shorelines](https://global-ecosystems.org/explore/groups/MT1.1)                  |
| Kelp forests                       |  `10` | Marine                        | Marine shelf   | M1.2  | [Kelp forests](https://global-ecosystems.org/explore/groups/M1.2)                       |

Every occurrence record in coastTrain includes the following attributes.

```
{
	"Type": feature,
	"ID": 1,
	"Lat": 37.607358205897143,
	"Lon": -122.114158970611470,
	"Class": 2,
	"Method": "image interpretation",
	"Scale": 30,
	"IUCN_Realm": "Marine-Terrestrial",
	"IUCN_Biome": "Shorelines Biome",
	"IUCN_Funct": "Muddy Shorelines",
	"IUCN_FunGC": "MT1.2",
	"RefDatSta": 2014,
	"RefDatEnd": 2016,
	"Proj_Ref": "GIC"
        "Ecosys_Typ": "Tidal Flat"
}
```

#### Acknowledgements
coastTrain was developed with an ARC Discovery Early Career Researcher Grant to Murray (DE190100101).

#### Example publications
Below is a set of papers that have used or supplied data to coastTrain.

*Coral reefs*

> Roelfsema, C.M., Borrego-Acevedo, R., Canto, R., Harris, D.' Kennedy, E.V., Kovacs, E., et al., 2021. Benthic and Geomorphic Reference Data for Global Coral Reef Mapping. figshare. Collection. https://doi.org/10.6084/m9.figshare.c.5233847.v6 

> Roelfsema, C.M., Lyons, M.B., Kovacs, E.M., Kennedy, E.V., Markey, K., Borrego-Acevedo, R., Alvarez Ordoñez, A., Say, C., Tudman, P., Roe, M. and Wolff, J., 2021. Workflow for the generation of expert-derived training and validation data: A view to global scale habitat mapping. Frontiers in Marine Science, 8, pp.1-13. https://doi.org/10.3389/fmars.2021.643381.

> B. Lyons, M., M. Roelfsema, C., V. Kennedy, E., M. Kovacs, E., Borrego‐Acevedo, R., Markey, K., Roe, M., M. Yuwono, D., L. Harris, D., R. Phinn, S. and Asner, G.P., 2020. Mapping the world's coral reefs using a global multiscale earth observation framework. Remote Sensing in Ecology and Conservation, 6(4), pp.557-568. https://doi.org/10.1002/rse2.157.

*Mangroves*
> Bunting, P., Rosenqvist, A., Hilarides, L., Lucas, R.M. and Thomas, N., 2022. Global Mangrove Watch: Updated 2010 Mangrove Forest Extent (v2. 5). Remote Sensing, 14(4), p.1034. https://doi.org/10.3390/rs14041034.

> Bunting, P., Rosenqvist, A., Hilarides, L., Lucas, R.M., Thomas, N., Tadono, T., Worthington, T.A., Spalding, M., Murray, N.J. and Rebelo, L.M., 2022. Global Mangrove Extent Change 1996–2020: Global Mangrove Watch Version 3.0. Remote Sensing, 14(15), p.3657. https://doi.org/10.3390/rs14153657.

> Bunting, P., Rosenqvist, A., Lucas, R.M., Rebelo, L.M., Hilarides, L., Thomas, N., Hardy, A., Itoh, T., Shimada, M. and Finlayson, C.M., 2018. The global mangrove watch—a new 2010 global baseline of mangrove extent. Remote Sensing, 10(10), p.1669. https://doi.org/10.3390/rs10101669.



*Tidal flats*
> Murray, N.J., Phinn, S.R., DeWitt, M., Ferrari, R., Johnston, R., Lyons, M.B., Clinton, N., Thau, D. and Fuller, R.A., 2019. The global distribution and trajectory of tidal flats. Nature, 565(7738), pp.222-225. https://doi.org/10.1038/s41586-018-0805-8. 

> Murray, N. J., Phinn, S. R., Fuller, R. A., DeWitt, M., Ferrari, R., Johnston, R., Clinton, N. & Lyons, M. B., 2022. High-resolution global maps of tidal flat ecosystems from 1984 to 2019. Scientific Data, 9(1), pp.1-9. https://doi.org/10.1038/s41597-022-01635-5.

> Murray, N.J., Worthington, T.A., Bunting, P., Duce, S., Hagger, V., Lovelock, C.E., Lucas, R., Saunders, M.I., Sheaves, M., Spalding, M. and Waltham, N.J., 2022. High-resolution mapping of losses and gains of Earth’s tidal wetlands. Science, 376(6594), pp.744-749. https://doi.org/10.1126/science.abm9583.


#### Version notes
`version 1.0` public release
