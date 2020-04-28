---
title: Раздел Schema (Справочник по базам данных Access на компьютере)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308941"
---
# <a name="schema-section"></a>Раздел схемы

**Область применения**: Access 2013, Office 2013

## <a name="schema-section"></a>Schema Section

Раздел схемы является обязательным. Как показано в предыдущем примере, ADO записывает подробные метаданные для каждого столбца, чтобы сохранить семантику значений данных, насколько это возможно для обновления. Однако для загрузки в XML для ADO требуются только имена столбцов и набор строк, к которым они относятся. Ниже приведен пример минимальной схемы:

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

В вышеприведенном случае ADO будет рассматривать данные как строки переменной длины, так как в схему не включены сведения о типе.

## <a name="creating-aliases-for-column-names"></a>Создание псевдонимов для имен столбцов

Атрибут **RS: Name** позволяет создать псевдоним для имени столбца, чтобы понятное имя отображалось в сведениях о столбцах, предоставляемых набором строк, и в разделе Data можно использовать более короткое имя. Например, приведенная выше схема может быть изменена для сопоставления Шипперид с S1, CompanyName — S2, а телефон — для S3 следующим образом:

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

Затем в разделе Data строка будет использовать атрибут **Name** (не **RS: Name**), чтобы ссылаться на этот столбец:

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

Создание псевдонимов для имен столбцов является обязательным, если имя столбца не является допустимым атрибутом или именем тега в XML. Например, "Last Name" должен иметь псевдоним, так как имена с вложенными пробелами являются недопустимыми атрибутами. Следующая строка не будет правильно обработана средством синтаксического анализа XML, поэтому необходимо создать псевдоним для другого имени, у которого нет внедренного пространства:

```xml 
 
<row last name="Jones"/> 
```

Любое значение, используемое для атрибута **Name** , должно постоянно использоваться в каждой позиции, на которую ссылается столбец, в схеме и в разделах данных XML-документа. В следующем примере показано согласованное использование S1:

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

Аналогично, так как псевдоним для CompanyName не определен, CompanyName должен использоваться единообразно во всем документе.

## <a name="data-types"></a>Типы данных

Вы можете применить тип данных к столбцу с атрибутом **DT: Type** . Вы можете указать тип данных двумя способами: либо укажите атрибут **DT: Type** непосредственно в самом определении столбца, либо используйте конструкцию **с:дататипе** в качестве вложенного элемента определения столбца. For example,

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

эквивалентно

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Если опустить атрибут **DT: Type** полностью из определения строки, то по умолчанию типом столбца будет строка переменной длины.

Если у вас больше сведений о типе, чем просто имя типа (например, **DT: MaxLength**), то для использования дочернего элемента **с:дататипе** становится более удобочитаемым. Тем не менее, это просто соглашение, а не требование.

В следующих примерах показано, как включить сведения о типах в схему:

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

Во втором примере используется незаметное использование атрибута **RS: фикседленгс** . Столбец с атрибутом **RS: фикседленгс** , для которого задано значение true, указывает, что длина данных должна быть определена в схеме. В этом случае допустимым значением идентификатора заголовка\_является "123456", как "123". Однако "123" не является допустимым, так как его длина равна 3, а не 6. Более полное описание свойства **фикседленгс** показано в руководстве программиста по OLE DB.

## <a name="handling-nulls"></a>Обработка значений NULL

Значения NULL обрабатываются атрибутом **RS: майбенулл** . Если для этого атрибута задано значение true, то содержимое столбца может содержать значение null. Кроме того, если столбец не найден в строке данных, то пользователь, считывающий данные из набора строк, будет получать значение NULL из элемента **IRowset:: GetData ()**. Обратите внимание на следующие определения столбцов из таблицы Поставщики.

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

Определение разрешает для CompanyName значение null, но Шипперид не может содержать значение null. Если раздел Data содержит следующую строку, то поставщик сохраняемости настроил состояние данных для столбца CompanyName на константу состояния OLE DB ДБСТАТУС\_S\_IsNull:

```xml 
 
<z:row ShipperID="1"/> 
```

Если строка была полностью пустой, то поставщик сохраняемости возвратит состояние OLE DB\_дбстатус E\_недоступно для шипперид и Дбстатус\_S\_IsNull для CompanyName.

```xml 
 
<z:row/>  
```

Обратите внимание, что строка нулевой длины не совпадает со значением NULL.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Для предыдущей строки поставщик сохраняемости будет возвращать состояние OLE DB ДБСТАТУС\_S\_ОК для обоих столбцов. В этом случае названием CompanyName является просто "" (строка нулевой длины).

Для получения дополнительных сведений о конструкциях OLE DB, доступных для использования в схеме XML-документа для OLE DB, ознакомьтесь с определением "urn: schemas-microsoft-com: RowSet" и руководством программиста по OLE DB.

