---
title: Иерархические наборы записей в XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0aafaa1f7f49d34d647ec0f733e68de21cb5369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292015"
---
# <a name="hierarchical-recordsets-in-xml"></a>Иерархические наборы записей в XML


**Область применения**: Access 2013, Office 2013

## <a name="hierarchical-recordsets-in-xml"></a>Иерархические наборы записей в XML

ADO позволяет сохранять иерархические объекты **Recordset** в XML. С **иерархическими объектами Recordset** значение поля в родительском **наборе записей** является еще одним **набором записей.** Такие поля представлены как детские элементы в XML-потоке, а не атрибут. В следующем примере показано следующее:

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

Ниже приводится XML-формат сохраняемого **набора записей:**

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

Точный порядок столбцов в родительском **наборе записей** не очевиден, если он сохраняется таким образом. Любое поле в родительском поле может содержать набор **записей для детей.** Поставщик сохраняемости сохраняет все столбцы scalar сначала в качестве  атрибутов, а затем сохраняет все "столбцы" наборов записей для детей в качестве детских элементов родительской строки. Ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset.** Каждое поле имеет свойство OLE DB **rs:number,** определенное в пространстве имен **схемы Recordset,** содержаще ordinal number для этого поля.

Имена всех полей в детском наборе **записей** согласуются с именем поля в родительском **Наборе** записей, содержаном этот ребенок. Это необходимо для того, чтобы не было столкновений  имен в случаях, когда родительские и детские записи содержат поле, полученное из двух разных таблиц, но именуется сингулярно.

При сохранении иерархических **записей** в XML следует помнить о следующих ограничениях в ADO:

  - Иерархический **набор записей с** ожидающих обновлений не может сохраняться в XML.

  - Иерархический **набор записей,** созданный с командой параметризированной формы, не может сохраняться (в формате XML или ADTG).

  - В настоящее время ADO сохраняет связь между родительским и ребенком **Recordsets** как двоичный большой объект (BLOB). XML-теги для описания этого отношения еще не определены в пространстве имен схемы rowset.

  - При сэкономлении иерархического **набора** записей все **наборы** записей для детей сохраняются вместе с ним. Если текущий **Набор записей** является ребенком другого **Recordset,** его родитель не сохранен. Сохраняются **все наборы** записей для детей, которые составляют подтрий текущего **набора** записей.

При повторном возобновлении иерархического **recordset** из формата XML-сохраняемого формата необходимо помнить о следующих ограничениях:

  - Если детская запись содержит записи, для которых нет соответствующих родительских записей, эти строки не записывают в XML-представлении иерархического **набора записей.** Таким образом, эти строки будут потеряны при повторном возобновлении **recordset** из сохраняемой расположения.

  - Если детская запись содержит ссылки на несколько родительских записей, то при повторном возобновлении **recordset** ребенок **Recordset** может содержать дублирующиеся записи. Однако эти дубликаты будут видны только в том случае, если пользователь работает непосредственно с указанным в ней набором детских строк. Если для навигации по детскому набору **записей** используется глава (это единственный способ навигации по ADO), дубликаты не видны.

