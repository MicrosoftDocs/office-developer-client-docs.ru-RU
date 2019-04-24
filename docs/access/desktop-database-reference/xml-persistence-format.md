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

ADO использует кодировку UTF-8 для XML-потока, который он сохраняет.

Формат ADO XML разбивается на два раздела: раздел схемы, за которым следует раздел Data. Ниже приведен пример XML-файла для таблицы грузоотправителей из базы данных Northwind. В этом примере рассматриваются различные части XML-кода.

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

В схеме показаны объявления пространств имен, раздела схемы и раздела данных. Раздел Schema содержит определения для строки, Шипперид, CompanyName и телефона.

Определения схемы соответствуют спецификации XML-данных и могут быть полностью проверены (хотя проверка не будет выполняться в Internet Explorer 5). Эту спецификацию можно просмотреть на странице [W3C по XMLDATA](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data — это единственный поддерживаемый формат схемы для сохраняемого **набора записей** в настоящее время.

Раздел данных содержит три строки, содержащие сведения о грузоотправителях. Для пустого набора строк раздел Data может быть пустым, но должны присутствовать `<rs:data>` Теги. Без данных вы можете написать сокращенную форму тега простым `<rs:data>`. Любой тег с префиксом RS указывает на то, что он находится в пространстве имен, определенном с помощью параметра urn: schemas-microsoft-com: Rowset. Полное определение этой схемы определено в приложении в этом документе.

## <a name="xml-persistence-format"></a>XML Persistence Format

ADO использует кодировку UTF-8 для XML-потока, который он сохраняет.

Формат ADO XML разбивается на два раздела: раздел схемы, за которым следует раздел Data. Ниже приведен пример XML-файла для таблицы грузоотправителей из базы данных Northwind. В этом примере рассматриваются различные части XML-кода.

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

В схеме показаны объявления пространств имен, раздела схемы и раздела данных. Раздел Schema содержит определения для строки, Шипперид, CompanyName и телефона.

Определения схемы соответствуют спецификации XML-данных и могут быть полностью проверены (хотя проверка не будет выполняться в Internet Explorer 5). Эту спецификацию можно просмотреть на странице [W3C по XMLDATA](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data — это единственный поддерживаемый формат схемы для сохраняемого **набора записей** в настоящее время.

Раздел данных содержит три строки, содержащие сведения о грузоотправителях. Для пустого набора строк раздел Data может быть пустым, но должны присутствовать `<rs:data>` Теги. Без данных вы можете написать сокращенную форму тега простым `<rs:data>`. Любой тег с префиксом RS указывает на то, что он находится в пространстве имен, определенном с помощью параметра urn: schemas-microsoft-com: Rowset. Полное определение этой схемы определено в приложении в этом документе.

