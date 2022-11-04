<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体。棋子  
=====<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.RoboticIndustrialActivities/blob/master/Piece/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全球描述。**待制造的一件物品。  
版本：0.0.2  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

##属性列表  

<sup><sub>[*] 如果一个属性中没有一个类型，是因为它可能有几种类型或不同的格式/模式</sub></sup>。  
- `address[object]`: 邮寄地址  . Model: [https://schema.org/address](https://schema.org/address)- `alternateName[string]`: 这个项目的一个替代名称  - `areaServed[string]`: 提供服务或提供项目的地理区域  . Model: [https://schema.org/Text](https://schema.org/Text)- `dataProvider[string]`: 一串识别统一数据实体提供者的字符。  - `dateCreated[string]`: 实体创建时间戳。这通常会由存储平台分配。  - `dateModified[string]`: 实体最后一次修改的时间戳。这通常会由存储平台分配。  - `description[string]`: 对这个项目的描述  - `id[*]`: 实体的唯一标识符  - `location[*]`: 对该项目的Geojson引用。它可以是点、线字符串、多边形、多点、多线字符串或多多边形。  - `manufacturabilityOnFlexEdge[string]`: 表示该件物品是否可以被机器人拿起并被处理。Enum:'canPickUpOnly, cannotPickUp, canProcess'（仅能拾取，不能拾取，能处理）。  - `name[string]`: 这个项目的名称。  - `owner[array]`: 一个包含JSON编码的字符序列的列表，引用所有者的唯一Ids。  - `pieceID[string]`: 该作品的名称  . Model: [https://schema.org/Text](https://schema.org/Text)- `refPieceLocation[*]`: 一个工件的当前位置，在机器人上，在托盘上，等等。  - `seeAlso[*]`: 指向有关该项目的其他资源的URI列表  - `sequenceNumber[number]`: 表示工件在托盘上的位置  . Model: [https://schema.org/Number](https://schema.org/Number)- `source[string]`: 一系列的字符，以URL的形式给出实体数据的原始来源。建议为源提供者的完全合格域名，或源对象的URL。  - `status[string]`: 表示项目的当前状态  . Model: [https://schema.org/Text](https://schema.org/Text)- `timeEstimatedOnFlexEdge[number]`: 估计处理该作品的时间为多少秒  . Model: [https://schema.org/Text](https://schema.org/Text)- `type[string]`: 它必须是件。NGSI实体类型。  - `weight[number]`: 表明物品的重量  . Model: [https://schema.org/Number](https://schema.org/Number)<!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## 数据模型的属性描述  
按字母顺序排列（点击查看详情）。  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
Piece:    
  description: 'A Piece to be manufactured.'    
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
      type: object    
      x-ngsi:    
        model: https://schema.org/address    
        type: Property    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
        type: Property    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: 'A description of this item'    
      type: string    
      x-ngsi:    
        type: Property    
    id:    
      anyOf: &piece_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Unique identifier of the entity'    
      x-ngsi:    
        type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: 'GeoProperty. Geojson reference to the item. Point'    
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
        - description: 'GeoProperty. Geojson reference to the item. LineString'    
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
        - description: 'GeoProperty. Geojson reference to the item. Polygon'    
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
        - description: 'GeoProperty. Geojson reference to the item. MultiPoint'    
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
        - description: 'GeoProperty. Geojson reference to the item. MultiLineString'    
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
        - description: 'GeoProperty. Geojson reference to the item. MultiLineString'    
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
      x-ngsi:    
        type: GeoProperty    
    manufacturabilityOnFlexEdge:    
      description: 'Indicates if the Piece can be picked up by robot and be processed. Enum:''canPickUpOnly, cannotPickUp, canProcess'''    
      enum:    
        - canPickUpOnly    
        - cannotPickUp    
        - canProcess    
      type: string    
      x-ngsi:    
        type: Property    
    name:    
      description: 'The name of this item.'    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *piece_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Property    
    pieceID:    
      description: 'The Id of the piece'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    refPieceLocation:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Current location of a piece, on robot, on pallet, etc.'    
      x-ngsi:    
        type: Relationship    
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
      x-ngsi:    
        type: Property    
    sequenceNumber:    
      description: 'Indicates the position of the piece on a pallet'    
      type: number    
      x-ngsi:    
        model: https://schema.org/Number    
        type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: string    
      x-ngsi:    
        type: Property    
    status:    
      description: 'Indicates the current status of the item'    
      enum:    
        - created    
        - inProcess    
        - finished    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    timeEstimatedOnFlexEdge:    
      description: 'Number of seconds it is estimated to process the piece'    
      type: number    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    type:    
      description: 'It has to be Piece. NGSI Entity type.'    
      enum:    
        - Piece    
      type: string    
      x-ngsi:    
        type: Property    
    weight:    
      description: 'Indicates the weight off the item'    
      type: number    
      x-ngsi:    
        model: https://schema.org/Number    
        type: Property    
  required:    
    - id    
    - type    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2021 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.RoboticIndustrialActivities/blob/master/Piece/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.RoboticIndustrialActivities/Pallet/schema.json    
  x-model-tags: ""    
  x-version: 0.0.2    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## ＃＃＃＃有效载荷的例子  
#### Piece NGSI-v2 key-values 示例  
这里有一个JSON-LD格式的Piece作为key-values的例子。当使用`options=keyValues`时，这与NGSI-v2兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "Piece.0001",  
  "type": "Piece",  
  "pieceID": "0001",  
  "dateCreated": "2018-09-27T12:00:00Z",  
  "manufacturabilityOnFlexEdge" : "canPickUpOnly",  
  "timeEstimatedOnFlexEdge": 600,  
  "weight" : 37,  
  "sequenceNumber": 1,  
  "refPieceLocation": "Robot.DuoCutRobot",  
  "status": "created"  
}   
```  
</details>  
#### Piece NGSI-v2规范化示例  
这里有一个JSON-LD格式的Piece的例子，是规范化的。当不使用选项时，这与NGSI-v2兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:Piece:0001",  
  "type": "Piece",  
  "pieceID": {  
    "type": "Text",  
    "value": "0001"  
  },  
  "dateCreated": {  
    "type" : "DateTime",  
    "value": "2018-09-27T12:00:00Z"  
  },  
  "manufacturabilityOnFlexEdge":{  
      "type" : "Text",  
      "value": "CanPickUpOnly"  
  },  
  "timeEstimatedOnFlexEdge": {  
    "type" : "Number",  
    "value": "600"  
  },  
  "weight": {  
    "type" : "Number",  
    "value": 37  
  },  
  "weight": {  
    "type" : "sequenceNumber",  
    "value": 1  
  },  
  "refpieceLocation": {  
    "type" : "Text",  
    "value": "urn:ngsi-ld:Robot:DuoCutRobot"  
  },  
  "status": {  
    "type" : "Text",  
    "value": "Created"  
  }  
}   
```  
</details>  
#### 件NGSI-LD密钥值示例  
这里有一个JSON-LD格式的Piece作为key-values的例子。当使用`options=keyValues`时，这与NGSI-LD兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:Piece:0001",  
    "type": "Piece",  
    "dateCreated": "2018-09-27T12:00:00Z",  
    "manufacturabilityOnFlexEdge": "canPickUpOnly",  
    "pieceID": "0001",  
    "refPieceLocation": "urn:ngsi-ld:Robot:DuoCutRobot",  
    "sequenceNumber": 1,  
    "status": "created",  
    "timeEstimatedOnFlexEdge": 600,  
    "weight": 37,  
    "@context": [  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.RoboticIndustrialActivities/master/context.jsonld"  
    ]  
}  
```  
</details>  
#### Piece NGSI-LD归一化的例子  
这里有一个JSON-LD格式的Piece的例子，是规范化的。当不使用选项时，这与NGSI-LD兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:Piece:0001",  
    "type": "Piece",  
    "dateCreated": {  
        "type": "Property",  
        "value": {  
            "@type": "DateTime",  
            "@value": "2018-09-27T12:00:00Z"  
        }  
    },  
    "manufacturabilityOnFlexEdge": {  
        "type": "Property",  
        "value": "CanPickUpOnly"  
    },  
    "pieceID": {  
        "type": "Property",  
        "value": "0001"  
    },  
    "refPieceLocation": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:Robot:DuoCutRobot"  
    },  
    "sequenceNumber": {  
        "type": "Property",  
        "value": 1  
    },  
    "status": {  
        "type": "Property",  
        "value": "Created"  
    },  
    "timeEstimatedOnFlexEdge": {  
        "type": "Property",  
        "value": "600"  
    },  
    "weight": {  
        "type": "Property",  
        "value": 37  
    },  
    "@context": [  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.RoboticIndustrialActivities/master/context.jsonld"  
    ]  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
参见[常见问题10](https://smartdatamodels.org/index.php/faqs/)，以获得关于如何处理量级单位的答案。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
