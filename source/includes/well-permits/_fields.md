# Well Permits

## Fields

Below describes the well permit interface and expected fields.

### Meter Reading Fields

```ts
interface WellPermit {
  asBuiltAquifers?: string; // As Built Aquifers
  associatedAquifers?: string; // Associated Aquifers
  associatedCaseNumbers?: string; // Water court case number(s) associated with water right
  associatedUses?: string; // Associated Uses
  bottomPerforatedCasing?: number; // Depth from surface to bottom of perforated casing (feet)
  contactAddress?: string; // Contact Address
  contactCity?: string; // Contact City
  contactName?: string; // Contact Name
  contactPostalCode?: string; // Contact Postal Code
  contactStateOrProvince?: string; // Contact State Or Province
  contactType?: string; // Contact Type
  coordsEw?: number; // Distance and direction from East/West section line (feet)
  coordsEwDir?: string; // Direction of measurement from East/West section line
  coordsNs?: number; // Distance and direction from North/South section line (feet)
  coordsNsDir?: string; // Direction of measurement from North/South section line
  county?: string; // County where the well is located
  date1stBeneficialUse?: Date; // Date of First Beneficial Use
  dateApplicationReceived?: Date; // Date Application Received
  datePermitExpires?: Date; // Date Permit Expires
  datePermitIssued?: Date; // Date Permit Issued
  datePumpInstalled?: Date; // Date Pump Installed
  dateWellCompleted?: Date; // Date Well Completed
  dateWellPlugged?: Date; // Date Well Plugged
  denverBasinAquifer?: string; // Denver Basin Aquifer
  depthTotal?: number; // Depth Total (ft)
  designatedBasinName?: string; // Eight established geographic areas in Colorado's Eastern Plains where users rely primarily on groundwater for water supply
  division?: number; // DWR Water Division
  driller?: string; // Driller
  drillerLic?: string; // Driller License
  elevation?: number; // Elevation (ft)
  latitude?: number; // Latitude value in decimal degrees
  locationAccuracy?: string; // Accuracy of location coordinates
  locationType?: string; // Location Type
  longitude?: number; // Longitude (decimal degrees)
  managementDistrictName?: string; // Thirteen local districts, within the Designated Basins, with additional administrative authority
  modified?: Date; // Last date time that this record was modified in the DWR database
  moreInformation?: string; // Hyperlink to additional details
  parcelName?: string; // Parcel Name
  permit: string; // Well permit number
  permitCategoryDescr?: string; // Permit Category Description
  permitCurrentStatusDescr?: string; // Permit Current Status Description
  physicalAddress?: string; // Physical Address
  physicalCity?: string; // Physical City
  physicalPostalCode?: string; // Physical Postal Code
  physicalStateOrProvince?: string; // Physical State Or Province
  pm?: string; // Principal Meridian of well’s legal location - there are 5 principal meridians in CO?: Sixth (S), New Mexico (N), Baca (B), Costilla (C), and Ute (U)
  pumpInstaller?: string; // Pump Installer
  pumpLic?: string; // Pump License
  pumpTestYield?: number; // Pump Test Yield
  q10?: string; // Legal location?: 10 acre quarter section
  q160?: string; // Legal location?: 160 acre quarter section
  q40?: string; // Legal location?: 40 acre quarter section
  range?: string; // Legal location?: A number in the format “nnnd” where “nnn” is the range number and “d” is the direction either East or West
  receipt?: string; // Permit application receipt number
  section?: string; // Section number - township, range divided into 36 one square mile sections; “U” indicates location in Ute Correction (Division 7 only)
  staticWaterLevel?: number; // Static Water Level (ft)
  staticWaterLevelDate?: Date; // Static Water Level Date
  topPerforatedCasing?: number; // Depth from surface to top of perforated casing (feet)
  township?: string; // Legal location?: Township number and direction
  utmX?: number; // The x (Easting) component of the Universal Transverse Mercator system. (Zone 13, NAD83 datum)
  utmY?: number; // The y (Northing) component of the Universal Transverse Mercator system. (Zone 13, NAD83 datum)
  waterDistrict?: number; // DWR Water District
  wdid?: string; // DWR unique structure identifier
}
```

> Below is an example record in JSON

```json
{
  "associatedAquifers": "ALL UNNAMED AQUIFERS",
  "associatedUses": "Other",
  "contactAddress": "12 A1 PHILLIPS BUILDING",
  "contactCity": "BARTLESVILLE",
  "contactName": "PHILLIPS PETROLEUM CO",
  "contactPostalCode": "74004",
  "contactStateOrProvince": "OK",
  "contactType": "Owner",
  "coordsEw": 2130,
  "coordsEwDir": "W",
  "coordsNs": 120,
  "coordsNsDir": "N",
  "county": "WELD",
  "dateWellPlugged": "1995-07-18T00:00:00",
  "denverBasinAquifer": "Yes",
  "designatedBasinName": "LOST CREEK",
  "division": 1,
  "latitude": 40.130818,
  "locationAccuracy": "Spotted from section lines",
  "locationType": "Well (Application/Permit)",
  "longitude": -104.406467,
  "managementDistrictName": "LOST CREEK",
  "modified": "2012-11-05T00:00:00",
  "moreInformation": "https://dwr.state.co.us/Tools/WellPermits/0000371B",
  "permit": "1995215-AB",
  "permitCategoryDescr": "Unknown",
  "permitCurrentStatusDescr": "Well Abandoned",
  "pm": "S",
  "q160": "NW",
  "q40": "NE",
  "range": "63.0 W",
  "receipt": "0000371B",
  "section": "23",
  "township": "2.0 N",
  "utmX": 550568.2,
  "utmY": 4442445.4,
  "waterDistrict": 1,
  "wdid": ""
}
```

| Property                 | Type   | Restrictions | Description                                                                                                                                         |
| ------------------------ | ------ | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| permit                   | string | required     | Well permit number                                                                                                                                  |
| receipt                  | string | required     | Permit application receipt number                                                                                                                   |
| contactName              | string | required     | Contact Name                                                                                                                                        |
| asBuiltAquifers          | string | optional     | As Built Aquifers                                                                                                                                   |
| associatedAquifers       | string | optional     | Associated Aquifers                                                                                                                                 |
| associatedCaseNumbers    | string | optional     | Water court case number(s) associated with water right                                                                                              |
| associatedUses           | string | optional     | Associated Uses                                                                                                                                     |
| bottomPerforatedCasing   | number | optional     | Depth from surface to bottom of perforated casing (feet)                                                                                            |
| contactAddress           | string | optional     | Contact Address                                                                                                                                     |
| contactCity              | string | optional     | Contact City                                                                                                                                        |
| contactPostalCode        | string | optional     | Contact Postal Code                                                                                                                                 |
| contactStateOrProvince   | string | optional     | Contact State Or Province                                                                                                                           |
| contactType              | string | optional     | Contact Type                                                                                                                                        |
| coordsEw                 | number | optional     | Distance and direction from East/West section line (feet)                                                                                           |
| coordsEwDir              | string | optional     | Direction of measurement from East/West section line                                                                                                |
| coordsNs                 | number | optional     | Distance and direction from North/South section line (feet)                                                                                         |
| coordsNsDir              | string | optional     | Direction of measurement from North/South section line                                                                                              |
| county                   | string | optional     | County where the well is located                                                                                                                    |
| date1stBeneficialUse     | Date   | optional     | Date of First Beneficial Use                                                                                                                        |
| dateApplicationReceived  | Date   | optional     | Date Application Received                                                                                                                           |
| datePermitExpires        | Date   | optional     | Date Permit Expires                                                                                                                                 |
| datePermitIssued         | Date   | optional     | Date Permit Issued                                                                                                                                  |
| datePumpInstalled        | Date   | optional     | Date Pump Installed                                                                                                                                 |
| dateWellCompleted        | Date   | optional     | Date Well Completed                                                                                                                                 |
| dateWellPlugged          | Date   | optional     | Date Well Plugged                                                                                                                                   |
| denverBasinAquifer       | string | optional     | Denver Basin Aquifer                                                                                                                                |
| depthTotal               | number | optional     | Depth Total (ft)                                                                                                                                    |
| designatedBasinName      | string | optional     | Eight established geographic areas in Colorado's Eastern Plains where users rely primarily on groundwater for water supply                          |
| division                 | number | optional     | DWR Water Division                                                                                                                                  |
| driller                  | string | optional     | Driller                                                                                                                                             |
| drillerLic               | string | optional     | Driller License                                                                                                                                     |
| elevation                | number | optional     | Elevation (ft)                                                                                                                                      |
| latitude                 | number | optional     | Latitude value in decimal degrees                                                                                                                   |
| locationAccuracy         | string | optional     | Accuracy of location coordinates                                                                                                                    |
| locationType             | string | optional     | Location Type                                                                                                                                       |
| longitude                | number | optional     | Longitude (decimal degrees)                                                                                                                         |
| managementDistrictName   | string | optional     | Thirteen local districts, within the Designated Basins, with additional administrative authority                                                    |
| modified                 | Date   | optional     | Last date time that this record was modified in the DWR database                                                                                    |
| moreInformation          | string | optional     | Hyperlink to additional details                                                                                                                     |
| parcelName               | string | optional     | Parcel Name                                                                                                                                         |
| permitCategoryDescr      | string | optional     | Permit Category Description                                                                                                                         |
| permitCurrentStatusDescr | string | optional     | Permit Current Status Description                                                                                                                   |
| physicalAddress          | string | optional     | Physical Address                                                                                                                                    |
| physicalCity             | string | optional     | Physical City                                                                                                                                       |
| physicalPostalCode       | string | optional     | Physical Postal Code                                                                                                                                |
| physicalStateOrProvince  | string | optional     | Physical State Or Province                                                                                                                          |
| pm                       | string | optional     | Principal Meridian of well’s legal location - there are 5 principal meridians in CO: Sixth (S), New Mexico (N), Baca (B), Costilla (C), and Ute (U) |
| pumpInstaller            | string | optional     | Pump Installer                                                                                                                                      |
| pumpLic                  | string | optional     | Pump License                                                                                                                                        |
| pumpTestYield            | number | optional     | Pump Test Yield                                                                                                                                     |
| q10                      | string | optional     | Legal location: 10 acre quarter section                                                                                                             |
| q160                     | string | optional     | Legal location: 160 acre quarter section                                                                                                            |
| q40                      | string | optional     | Legal location: 40 acre quarter section                                                                                                             |
| range                    | string | optional     | Legal location: A number in the format “nnnd” where “nnn” is the range number and “d” is the direction either East or West                          |
| section                  | string | optional     | Section number - township, range divided into 36 one square mile sections; “U” indicates location in Ute Correction (Division 7 only)               |
| staticWaterLevel         | number | optional     | Static Water Level (ft)                                                                                                                             |
| staticWaterLevelDate     | Date   | optional     | Static Water Level Date                                                                                                                             |
| topPerforatedCasing      | number | optional     | Depth from surface to top of perforated casing (feet)                                                                                               |
| township                 | string | optional     | Legal location: Township number and direction                                                                                                       |
| utmX                     | number | optional     | The x (Easting) component of the Universal Transverse Mercator system. (Zone 13, NAD83 datum)                                                       |
| utmY                     | number | optional     | The y (Northing) component of the Universal Transverse Mercator system. (Zone 13, NAD83 datum)                                                      |
| waterDistrict            | number | optional     | DWR Water District                                                                                                                                  |
| wdid                     | string | optional     | DWR unique structure identifier                                                                                                                     |
