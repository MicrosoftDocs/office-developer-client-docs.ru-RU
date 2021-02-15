---
title: Раздел схемы (справочник по базе данных Access для настольных ПК)
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

Раздел схемы является обязательной. Как показано в предыдущем примере, ADO записывает подробные метаданные о каждом столбце, чтобы сохранить семантику значений данных как можно больше для обновления. Однако для загрузки в XML ADO требуются только имена столбцов и набор строк, к которым они принадлежат. Вот пример минимальной схемы:

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

В вышеуказанной ситуации ADO будет рассматривать данные как строки переменной длины, так как в схему не включены сведения о типе.

## <a name="creating-aliases-for-column-names"></a>Создание псевдонимов для имен столбцов

Атрибут **rs:name** позволяет создать псевдоним для имени столбца, чтобы в сведениях о столбцах, которые кажутся в наборе строк, может отображаться удобное имя, а в разделе данных может использоваться более короткое имя. Например, схему выше можно изменить, чтобы соотоставить ShipperID с s1, CompanyName с s2 и Phone на s3 следующим образом:

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

Затем в разделе данных строка будет использовать атрибут **name** (не **rs:name)** для ссылки на этот столбец:

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

Создание псевдонимов для имен столбцов необходимо, если имя столбца не является юридическим атрибутом или именем тега в XML. Например, "Фамилия" должна иметь псевдоним, так как имена с внедренными пробелами являются запрещенными атрибутами. Следующая строка не будет правильно обработана синтакс помощью синтаксика XML, поэтому необходимо создать псевдоним для другого имени, которое не имеет встроенного пространства:

```xml 
 
<row last name="Jones"/> 
```

Любое значение, используемое для атрибута **name,** должно использоваться согласованно в каждом месте, на который ссылается столбец в разделах схемы и данных XML-документа. В следующем примере показано согласованное использование s1:

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

Аналогичным образом, так как псевдоним для CompanyName не определен выше, CompanyName необходимо использовать согласованно во всем документе.

## <a name="data-types"></a>Типы данных

Тип данных можно применить к столбце с атрибутом **dt:type.** Тип данных можно указать двумя способами: укажите атрибут **dt:type** непосредственно в самом определении столбца или используйте конструкцию **s:datatype** в качестве вложенного элемента определения столбца. Пример.

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

эквивалентен

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Если опустить атрибут **dt:type** полностью из определения строки, по умолчанию тип столбца будет переменной длиной строки.

Если у вас больше сведений о типе, чем просто имя типа (например, **dt:maxLength),** это делает его более учитаемым для использования **элемента s:datatype.** Однако это просто соглашение, а не требование.

В следующих примерах покажем, как включить сведения о типе в схему:

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

Во втором примере атрибут **rs:fixedlength** используется неявно. Столбец с **атрибутом rs:fixedlength,** установленным как true, означает, что данные должны иметь длину, определяемую в схеме. В этом случае юридическим значением для ид заголовка является \_ "123456", как "123." Однако "123" будет не допустимым, так как его длина составляет 3, а не 6. Более полное описание свойства **fixedlength** см. в руководстве программиста OLE DB.

## <a name="handling-nulls"></a>Обработка NULL

Значения NULL обрабатываются атрибутом **rs:maybenull.** Если для этого атрибута установлено значение true, содержимое столбца может содержать значение null. Кроме того, если столбец не найден в строке данных, пользователь, считывав данные из наборов строк, получит состояние NULL из **IRowset::GetData()**. Рассмотрим следующие определения столбцов из таблицы Shippers:

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

Определение позволяет companyName иметь значение null, но ShipperID не может содержать значение null. Если в разделе данных содержится следующая строка, поставщик сохраняемости будет устанавливать состояние данных для столбца CompanyName в константе состояния OLE DB DB DBSTATUS \_ S \_ ISNULL:

```xml 
 
<z:row ShipperID="1"/> 
```

Если строка была полностью пустой, то поставщик сохраняемости возвратит состояние OLE DB DB DB \_ \_ UNAVAILABLE для ShipperID и DBSTATUS S ISNULL для \_ \_ CompanyName.

```xml 
 
<z:row/>  
```

Обратите внимание, что строка нулевой длины не является нулевой.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

В предыдущей строке поставщик сохраняемости возвращает состояние OLE DB DB DBSTATUS \_ S \_ OK для обоих столбцов. В данном случае companyName — это просто "" (строка нулевой длины).

Дополнительные сведения о конструкциях OLE DB, доступных для использования в схеме XML-документа для OLE DB, см. в определении "urn:schemas-microsoft-com:rowset" и руководстве программиста OLE DB.

