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

ADO позволяет сохранять иерархические объекты **Recordset** в XML. При иерархических **объектах Recordset** значение поля в родительском наборе **записей является** другим **объектом Recordset.** Такие поля представлены в потоке XML в качестве не атрибута, а в качестве элементов. Этот пример демонстрируется в следующем примере:

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

Ниже приводится формат XML сохраняемого **наборов записей:**

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

Точный порядок столбцов в родительском наборе **записей** не является очевидным, если он сохраняется таким образом. Любое поле в родительском может содержать набор **записей.** Поставщик сохраняемости сначала сохраняет все скалярные столбцы в  качестве атрибутов, а затем сохраняет все "столбцы" наборов записей в качестве элементов родительской строки. Порядковую позицию поля в  родительском наборе записей можно получить, изсмотрев определение схемы **для recordset.** Каждое поле имеет свойство OLE DB **rs:number,** определенное в пространстве имен схемы **Recordset,** которое содержит порядковые номера для этого поля.

Имена всех полей в  этом наборе записей совмещены  с именем поля в родительском наборе записей, который содержит этот child. Это гарантирует отсутствие столкновений имен в случаях, когда  родительский и родительский записи содержат поле, полученное из двух разных таблиц, но именуется в единственном числе.

При сохранении иерархических **записей** в XML следует учитывать следующие ограничения в ADO:

  - Иерархический набор **записей с** ожидающих обновлений нельзя сохранить в XML.

  - Иерархический набор **записей,** созданный с помощью параметризованной команды фигуры, нельзя сохранить (в формате XML или ADTG).

  - В настоящее время ADO сохраняет отношение между родительским и потомком **Recordsets** как большой двоичный объект (BLOB). XML-теги для описания этой связи еще не определены в пространстве имен схемы наборов строк.

  - При сохранении иерархического **наборов** записей вместе с ним сохраняются все его наборы записей.  Если текущий **набор записей является** child of another **Recordset,** его родительский набор не будет сохранен. Сохраняются **все наборы записей,** которые формируют подпотее текущего **наборов** записей.

При повторном **повторном** открытие иерархического наборов записей из формата, сохраняемого в XML, необходимо помнить о следующих ограничениях:

  - Если родительская запись содержит записи, для которых нет соответствующих родительских записей, эти строки не записываюются в XML-представлении иерархического **наборов записей.** Таким образом, эти строки будут потеряны при повторном повторном открытие **наборе записей** из его сохраняемой области.

  - Если у родительской записи есть ссылки на несколько родительских записей, то при повторном подмножество записей может содержать повторяющиеся записи.  Однако эти дубликаты будут видны только в том случае, если пользователь работает непосредственно с этим набором строк. Если для навигации по  набору записей (единственный способ навигации по ADO) используется глава, дубликаты не видны.

