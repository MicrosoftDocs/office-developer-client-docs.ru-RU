---
title: XML Persistence Format
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7825d55c6f0c2f900f61a325265dce048f965e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308283"
---
# <a name="xml-persistence-format"></a>Формат сохранения XML

**Область применения**: Access 2013, Office 2013

## <a name="xml-persistence-format"></a>XML Persistence Format

ADO использует кодику UTF-8 для XML-потока, который он сохраняет.

Формат ADO XML разбивается на два раздела: раздел схемы, за которым следует раздел данных. Ниже приводится пример XML-файла для таблицы Shippers из базы данных Northwind. Далее в примере обсуждаются различные части XML.

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

Схема отображает объявления пространств имен, раздел схемы и раздел данных. Раздел схемы содержит определения строк, ShipperID, CompanyName и Phone.

Определения схемы соответствуют спецификации XML-Data и могут быть полностью проверены (хотя проверка не будет происходить в Internet Explorer 5). Эту спецификацию можно просмотреть в заметке [W3C XMLData.](https://www.w3.org/TR/1998/NOTE-XML-data-0105/) XML-Data это единственный поддерживаемый в настоящее время формат схемы **для сохраняемости Recordset.**

Раздел данных содержит три строки, содержащие сведения о поставках. Для пустого ряда раздел данных может быть пустым, но `<rs:data>` теги должны присутствовать. Без данных можно написать ярлык тега как просто `<rs:data>` . Любой тег с префиксом "rs" указывает, что он находится в пространстве имен, определяемом urn:schemas-microsoft-com:rowset. Полное определение этой схемы определено в приложении к данному документу.

## <a name="xml-persistence-format"></a>XML Persistence Format

ADO использует кодику UTF-8 для XML-потока, который он сохраняет.

Формат ADO XML разбивается на два раздела: раздел схемы, за которым следует раздел данных. Ниже приводится пример XML-файла для таблицы Shippers из базы данных Northwind. Далее в примере обсуждаются различные части XML.

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

Схема отображает объявления пространств имен, раздел схемы и раздел данных. Раздел схемы содержит определения строк, ShipperID, CompanyName и Phone.

Определения схемы соответствуют спецификации XML-Data и могут быть полностью проверены (хотя проверка не будет происходить в Internet Explorer 5). Эту спецификацию можно просмотреть в заметке [W3C XMLData.](https://www.w3.org/TR/1998/NOTE-XML-data-0105/) XML-Data это единственный поддерживаемый в настоящее время формат схемы **для сохраняемости Recordset.**

Раздел данных содержит три строки, содержащие сведения о поставках. Для пустого ряда раздел данных может быть пустым, но `<rs:data>` теги должны присутствовать. Без данных можно написать ярлык тега как просто `<rs:data>` . Любой тег с префиксом "rs" указывает, что он находится в пространстве имен, определяемом urn:schemas-microsoft-com:rowset. Полное определение этой схемы определено в приложении к данному документу.

