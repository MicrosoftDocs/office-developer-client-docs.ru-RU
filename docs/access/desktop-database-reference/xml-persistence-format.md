---
title: Формат сохранения XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 291a75fb88690a5674d872f2adb01b683f5e99bd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946715"
---
# <a name="xml-persistence-format"></a>Формат сохранения XML

**Применимо к**: Access 2013, Office 2013

## <a name="xml-persistence-format"></a>Формат сохранения XML

В ADO используется кодировка UTF-8 для потока XML, который она повторяется.

Формат ADO XML разбивается на два раздела, раздел схемы, а затем в разделе данных. Ниже приведен пример XML-файла в таблице «Поставщики» из базы данных Northwind. Различные части XML-код, обсуждаются в следующем примере.

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

Схема показано объявление пространства имен, в разделе схемы и в разделе данных. В разделе схема содержит определения для строки, ShipperID, название организации и телефон.

Определения схемы соответствуют спецификации XML-данных и могут быть полностью Подтверждено (Хотя проверка не будет выполнена в Internet Explorer 5). Можно просматривать спецификация [W3C XMLData Примечание](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-данных в настоящее время является формат только поддерживаемые схемы для сохранения **записей** .

В разделе данных имеет три строки, содержащие сведения о них. Для пустой набор строк, в разделе данных может быть пустым, но `<rs:data>` теги, должно быть установлено. Без данных можно написать сокращение тег просто `<rs:data>`. Любой тег начинаются с «rs» указывает, что в пространстве имен, определенные в urn: schemas-microsoft-com:rowset. Полное определение схемы определяется в приложении к этому документу.

## <a name="xml-persistence-format"></a>Формат сохранения XML

В ADO используется кодировка UTF-8 для потока XML, который она повторяется.

Формат ADO XML разбивается на два раздела, раздел схемы, а затем в разделе данных. Ниже приведен пример XML-файла в таблице «Поставщики» из базы данных Northwind. Различные части XML-код, обсуждаются в следующем примере.

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

Схема показано объявление пространства имен, в разделе схемы и в разделе данных. В разделе схема содержит определения для строки, ShipperID, название организации и телефон.

Определения схемы соответствуют спецификации XML-данных и могут быть полностью Подтверждено (Хотя проверка не будет выполнена в Internet Explorer 5). Можно просматривать спецификация [W3C XMLData Примечание](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-данных в настоящее время является формат только поддерживаемые схемы для сохранения **записей** .

В разделе данных имеет три строки, содержащие сведения о них. Для пустой набор строк, в разделе данных может быть пустым, но `<rs:data>` теги, должно быть установлено. Без данных можно написать сокращение тег просто `<rs:data>`. Любой тег начинаются с «rs» указывает, что в пространстве имен, определенные в urn: schemas-microsoft-com:rowset. Полное определение схемы определяется в приложении к этому документу.

