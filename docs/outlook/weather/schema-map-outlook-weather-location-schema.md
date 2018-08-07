---
title: Карта схемы (схема местоположения погоды Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a5195ae-7905-477a-7818-9eb3bff64af0
description: В этом разделе показано определение схемы для схемы XML местоположения погоды Outlook.
ms.openlocfilehash: e3938385402d79d0ca2efbbd383a0726d1cf801f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812915"
---
# <a name="schema-map-outlook-weather-location-schema"></a><span data-ttu-id="db10e-103">Карта схемы (схема местоположения погоды Outlook)</span><span class="sxs-lookup"><span data-stu-id="db10e-103">Schema map (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="db10e-104">В этом разделе показано определение схемы для схемы XML местоположения погоды Outlook.</span><span class="sxs-lookup"><span data-stu-id="db10e-104">This topic shows the schema definition for the Outlook Weather Location XML Schema.</span></span>
  
```XML
<?xml version="1.0" ?>
<xs:schema
  attributeFormDefault="unqualified" elementFormDefault="qualified"
xmlns:xs="http://www.w3.org/2001/XMLSchema"
targetNamespace= "http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd"
xmlns="http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd"
>
  <!-- get weather location  -->
  <!-- example query: http://weather.service.msn.com/data.aspx?outputview=search&amp;weasearchstr=tsurumi -->
  
  <xs:element name="weatherdata">
    <xs:annotation>
      <xs:documentation>Defines the weather element.</xs:documentation>
    </xs:annotation>
    <xs:complexType>
      <xs:sequence>
        <xs:element name="weather" type="weatherType" maxOccurs="unbounded">
          <xs:annotation>
            <xs:documentation>Specifies the location to report weather on.</xs:documentation>
          </xs:annotation>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <xs:complexType name="weatherType">
    <xs:annotation>
      <xs:documentation> Defines the parameters about the weather conditions of a location.</xs:documentation>
    </xs:annotation>
    <xs:attribute name="weatherlocationname" type="xs:string" use="required">
      <xs:annotation>
        <xs:documentation>Specifies the name of the location.</xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="weatherlocationcode" type="xs:string" use="required">
      <xs:annotation>
        <xs:documentation>Specifies a code that is associated with the location to distinguish multiple locations with the same name. </xs:documentation>
      </xs:annotation>
    </xs:attribute>
  </xs:complexType>
</xs:schema>
```


