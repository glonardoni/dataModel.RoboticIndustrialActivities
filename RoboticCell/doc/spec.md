Entity: RoboticCell  
===================  
[Open License](https://github.com/smart-data-models//dataModel.RoboticIndustrialActivities/blob/master/RoboticCell/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
Global description: **A Robotic cell.**  

## List of properties  

- `address`: The mailing address  - `alternateName`: An alternative name for this item  - `areaServed`: The geographic area where a service or offered item is provided  - `currentPieceNumber`:  Current number of pieces done in the job executing on the robotic cell.  - `dataProvider`: A sequence of characters identifying the provider of the harmonised data entity.  - `dateCreated`: Entity creation timestamp. This will usually be allocated by the storage platform.  - `dateModified`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.  - `description`: A description of this item  - `errorMessage`: The error message corresponding to the error number.  - `errorNumber`: Indicates if there if an error (value not 0) occurred on the cell.  - `id`: Unique identifier of the entity  - `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon  - `name`: The name of this item.  - `owner`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)  - `refIncomingPallet`: List of pallets providing incoming pieces for the cell.  - `refOutgoingPallet`: List of pallets providing outcoming pieces for the cell.  - `refRobot`: Robot belonging to the cell.  - `refVacuumPump`: Vacuum pump belonging to the cell.  - `seeAlso`: list of uri pointing to additional resources about the item  - `source`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.  - `totalNumberOfPieces`: Total number of pieces in the job executing on the robotic cell.  - `type`: It has to be RoboticCell. NGSI Entity type.    
Required properties  
- `id`  - `type`  ## Data Model description of properties  
Sorted alphabetically (click for details)  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
RoboticCell:    
  description: 'A Robotic cell.'    
  properties:    
    address:    
      description: 'The mailing address'    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, 03578. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, 24004. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
      type: Property    
      x-ngsi:    
        model: https://schema.org/address    
    alternateName:    
      description: 'An alternative name for this item'    
      type: Property    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    currentPieceNumber:    
      description: ' Current number of pieces done in the job executing on the robotic cell.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    description:    
      description: 'A description of this item'    
      type: Property    
    errorMessage:    
      description: 'The error message corresponding to the error number.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    errorNumber:    
      description: 'Indicates if there if an error (value not 0) occurred on the cell.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    id:    
      anyOf: &roboticcell_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Unique identifier of the entity'    
      type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: 'Geoproperty. Geojson reference to the item. Point'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Point'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. LineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON LineString'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. Polygon'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Polygon'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiPoint'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPoint'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiLineString'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPolygon'    
          type: object    
      type: Geoproperty    
    name:    
      description: 'The name of this item.'    
      type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *roboticcell_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: Property    
    refIncomingPallet:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'List of pallets providing incoming pieces for the cell.'    
      type: Relationship    
      x-ngsi:    
        model: https://schema.org/Text    
    refOutgoingPallet:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'List of pallets providing outcoming pieces for the cell.'    
      type: Relationship    
      x-ngsi:    
        model: https://schema.org/Text    
    refRobot:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Robot belonging to the cell.'    
      type: Relationship    
      x-ngsi:    
        model: https://schema.org/Text    
    refVacuumPump:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Vacuum pump belonging to the cell.'    
      type: Relationship    
      x-ngsi:    
        model: https://schema.org/Text    
    seeAlso:    
      description: 'list of uri pointing to additional resources about the item'    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: Property    
    totalNumberOfPieces:    
      description: 'Total number of pieces in the job executing on the robotic cell.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    type:    
      description: 'It has to be RoboticCell. NGSI Entity type.'    
      enum:    
        - RoboticCell    
      type: Property    
  required:    
    - id    
    - type    
  type: object    
```  
</details>    
## Example payloads    
#### RoboticCell NGSI-v2 key-values Example    
Here is an example of a RoboticCell in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
```json  
{  
  "id": "RoboticCell.FlexEdge",  
  "type": "RoboticCell",  
  "refRobot": "Robot.FlexEdgeRobot",  
  "refVacuumPump": "VacuumPump,FlexEdgePump",  
  "refIncomingPallet": "Pallet.0003",  
  "refOutgoingPallet": "Pallet.0004",  
  "errorNumber": 0,  
  "errorMessage": "",  
  "totalNumberOfPieces": 12,  
  "currentPieceNumber": 4  
}  
```  
#### RoboticCell NGSI-v2 normalized Example    
Here is an example of a RoboticCell in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
```json  
{  
  "id": "RoboticCell.FlexEdge",  
  "type": "RoboticCell",  
  "refRobot": {  
    "type": "Text",  
    "value": "Robot.FlexEdgeRobot"  
  },  
  "refVacuumPump": {  
    "type": "Text",  
    "value": "VacuumPump.FlexEdgePump"  
  },  
  "refIncomingPallet": {  
    "type": "Text",  
    "value": "Pallet.0003"  
  },  
  "refOutgoingPallet": {  
    "type": "Text",  
    "value": "Pallet.0004"  
  },  
  "errorNumber": {  
    "type": "Integer",  
    "value": 0  
  },  
  "errorMessage": {  
    "type": "Text",  
    "value": ""  
  },  
  "totalNumberOfPieces": {  
    "type": "Integer",  
	"value": 12  
  },  
  "currentPieceNumber": {  
    "type": "Integer",  
	"value": 4  
  }  
}  
```  
#### RoboticCell NGSI-LD key-values Example    
Here is an example of a RoboticCell in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
```json  
{  
  "id": "urn:ngsi-ld:RoboticCell:FlexEdge",  
  "type": "RoboticCell",  
  "refRobot": "urn:ngsi-ld:Robot:FlexEdgeRobot",  
  "refVacuumPump": "urn:ngsi-ld:VacuumPump:FlexEdgePump",  
  "refIncomingPallet": "urn:ngsi-ld:Pallet:0003",  
  "refOutgoingPallet": "urn:ngsi-ld:Pallet:0004",  
  "errorNumber": 0,  
  "errorMessage": "",  
  "totalNumberOfPieces": 12,  
  "currentPieceNumber": 4,  
  "@context": [  
    "https://smartdatamodels.org/context.jsonld"  
  ]  
}  
```  
#### RoboticCell NGSI-LD normalized Example    
Here is an example of a RoboticCell in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
```json  
{  
  "id": "urn:ngsi-ld:RoboticCell:FlexEdge",  
  "type": "RoboticCell",  
  "refRobot": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:Robot:FlexEdgeRobot"  
  },  
  "refVacuumPump": {  
    "type": "Relationship",  
    "object": "urn:ngsi-ld:VacuumPump:FlexEdgePump"  
  },  
  "refIncomingPallet": {  
    "type": "Relationship",  
    "object": "urn:ngsi-ld:Pallet:0003"  
  },  
  "refOutgoingPallet": {  
    "type": "Relationship",  
    "object": "urn:ngsi-ld:Pallet:0004"  
  },  
  "errorNumber": {  
    "type": "Property",  
    "value": 0  
  },  
  "errorMessage": {  
    "type": "Property",  
    "value": ""  
  },  
  "totalNumberOfPieces": {  
    "type": "Property",  
	"value": 12  
  },  
  "currentPieceNumber": {  
    "type": "Property",  
	"value": 4  
  },  
  "@context": [  
    "https://smartdatamodels.org/context.jsonld"  
  ]  
}  
```  
