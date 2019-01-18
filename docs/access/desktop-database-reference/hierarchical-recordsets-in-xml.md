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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709035"
---
# <a name="hierarchical-recordsets-in-xml"></a>Иерархические наборы записей в XML


**Применимо к**: Access 2013, Office 2013

## <a name="hierarchical-recordsets-in-xml"></a>Иерархические наборы записей в XML

ADO позволяет сохраняемость иерархических объектов **наборов записей** в XML. С объектами иерархических **записей** значение поля в родительском **записей** является другого **набора записей**. Такие поля, представленные в виде дочерних элементов в потоке XML, а не атрибут. В этом случае в следующем примере:

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

Ниже приведен XML-формат постоянных **набора записей**.

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

Порядок столбцов в родительской **записей** не очевидно, когда он сохраняется таким образом. Все поля в родительском может содержать дочерние **набора записей**. Поставщика службы сохранения сохраняется в работе все скалярные столбцы сначала как атрибуты и сохраняет выходной параметр все дочерние **записей** «столбцы» в качестве дочерних элементов родительской строки. Порядковый номер поля в родительском **записей** можно получить, посмотрев определение схемы **набора записей**. Каждое поле имеет свойство OLE DB **rs: номер**, определенные в пространстве имен схемы **набора записей** , который содержит порядковый номер для этого поля.

Имена всех полей в дочерних **записей** объединяются с именем поля в родительский **набор записей** , содержащий этот дочерний элемент. Это позволяет убедиться, что нет конфликтов имен в тех случаях, где родительских и дочерних **наборов записей** оба содержат поля, полученный из двух различных таблиц, но называется отдельности.

При сохранении иерархические **наборы записей** в формат XML, необходимо принять во внимание следующие ограничения в ADO:

  - Иерархическая **набора записей** с ожидающими обновлениями не могут быть сохранены в XML.

  - Иерархические **набора записей** , созданных с помощью команды параметризованный фигуры не могут быть сохранены (в формате XML или ADTG).

  - В настоящее время ADO сохраняет отношения между родительским и дочерним **наборов записей** в виде больших двоичных объектов (BLOB). XML-теги для описания отношение еще не были определены в пространстве имен схемы набора строк.

  - При сохранении иерархических **записей** всех дочерних **наборов записей** будут сохранены вместе с ним. Если текущего **набора записей** является дочерним элементом другого **набора записей**, его родителя не сохраняются. Все дочерние **наборы записей** , формирующие поддерева текущего **набора записей** будут сохранены.

При повторном открытии иерархических **записей** из формата XML сохраняются, необходимо принять во внимание следующие ограничения:

  - Если запись дочерних содержит записи, для которых нет соответствующих записей родительского, эти строки не записываются в XML-представление иерархических **набора записей**. Таким образом эти строки будут потеряны при повторном открытии **набора записей** из постоянных места.

  - Если дочерними есть ссылки на более одного родительской записи, затем при повторном открытии **набора записей**, дочерних **записей** может содержать повторяющихся записей. Тем не менее дубликаты будет только отображаться, если пользователь работает непосредственно с базового набора дочерних строк. Глава используется для перехода дочерних **записей** (это единственный способ перемещения по ADO), не видны дубликатов.

