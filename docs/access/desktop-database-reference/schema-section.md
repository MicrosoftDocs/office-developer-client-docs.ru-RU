---
title: Раздел схемы (Справочник по для настольных баз данных Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd1a67ebd992d90abf182c042bd3d68a6d0d4ce2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482589"
---
# <a name="schema-section"></a>Schema Section

**Применимо к**: Access 2013 | Office 2013

## <a name="schema-section"></a>Schema Section

В разделе Схема является обязательным. Как показано в предыдущем примере, ADO выводит подробные метаданных каждого столбца, чтобы сохранить как можно больше для обновления семантика значений данных. Тем не менее для загрузки в XML-КОДЕ ADO требуются только имена столбцов и строк, к которым они относятся. Ниже приведен пример минимальной схемы:

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

В случае выше ADO рассматривать данные как строки переменной длины, так как нет информации о типах включен в схеме.

## <a name="creating-aliases-for-column-names"></a>Создание псевдонимов для имен столбцов

Атрибут **rs: имя** позволяет создать псевдоним для имени столбца, чтобы это понятное имя может отображаться в столбец сведения, предоставляемые элементом набор строк и более короткое имя могут быть использованы в разделе данных. Например схемы, указанной выше может быть изменено сопоставьте ShipperID s1 CompanyName для s2, и номера на s3 следующим образом:

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

Затем в разделе данных строки использовать атрибут **name** (не **rs: имя**) для ссылки на этот столбец:

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

Создание псевдонимов для имен столбцов является обязательным, каждый раз, когда имя столбца не является допустимым именем атрибут или тега в формате XML. Например, «Фамилия» имеет псевдоним из-за незаконную атрибуты имен с пробелы. Следующая строка больше не обрабатывается правильно средство синтаксического анализа XML, поэтому необходимо создать псевдоним для другое имя, для которого не пробелы:

```xml 
 
<row last name="Jones"/> 
```

Любое значение, используйте для атрибута **name** должен использоваться постоянно на каждом месте, что ссылку на столбец в разделах схема и данные XML-документа. В следующем примере показано согласованное использование s1:

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

Аналогично поскольку псевдоним, не заданных для CompanyName выше, CompanyName должен использоваться постоянно в документе.

## <a name="data-types"></a>Типы данных

Тип данных можно применять в столбец с помощью атрибута **dt:type** . Тип данных можно указать двумя способами: Укажите атрибут **dt:type** непосредственно на определение столбца самого или использовать конструкцию **s:datatype** в качестве вложенного элемента определение столбца. Например:

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

соответствует

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Если опустить атрибут **dt:type** из определения строки по умолчанию, тип столбца будет строка переменной длины.

Если у вас есть Дополнительные сведения о типе, чем просто имя типа (например, **dt:maxLength**), становится более удобным для чтения, чтобы использовать дочерний элемент **s:datatype** . Это просто соглашение, тем не менее и не является обязательным требованием.

В приведенных ниже примерах Далее показано, как для включения информации о типах в схеме:

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

Существует тонкой использования атрибута **rs: fixedlength** во втором примере. Столбец с помощью атрибута **rs: fixedlength** значение true означает, что данные должны иметь длину, определенном в схеме. В этом случае юридическом значение для заголовка\_идентификатор является «123456», как «123». Тем не менее «123» не будет допустимым, так как его длина 3, не 6. В руководстве программиста OLE DB для более полное описание свойства **fixedlength** .

## <a name="handling-nulls"></a>Обработка значения NULL

Пустые значения обрабатываются в атрибуте **rs: maybenull** . Если этот атрибут имеет значение true, содержимое столбца может содержать значение null. Кроме того Если столбец не найден в строку данных, пользователь, чтение данных из строк получит значение null, состояние из **IRowset::GetData()**. Рассмотрим следующие определения столбца из таблицы «Поставщики».

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

Определение позволяет CompanyName должен иметь значение null, но ShipperID не может содержать значение null. В разделе данных содержит следующие строки, поставщика службы сохранения установить состояние данных для столбца CompanyName значение состояния OLE DB константу DBSTATUS\_S\_ISNULL:

```xml 
 
<z:row ShipperID="1"/> 
```

Если строка совершенно пустым, как показано ниже, поставщика службы сохранения вернет статус OLE DB DBSTATUS\_E\_НЕДОСТУПЕН для ShipperID и DBSTATUS\_S\_ISNULL для CompanyName.

```xml 
 
<z:row/>  
```

Обратите внимание на то, что строка нулевой длины не то же, что значение null.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Для предыдущего строки поставщика службы сохранения Возвращает статус OLE DB DBSTATUS\_S\_ОК для обоих столбцов. Имя компании в данном случае — это просто «» (строка нулевой длины).

Для дополнительных сведений о OLE DB создает доступным для использования в схеме XML-документа для OLE DB, просмотреть определение «urn: schemas-microsoft-com:rowset» и руководство программиста OLE DB.

