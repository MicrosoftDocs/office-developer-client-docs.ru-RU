---
title: Сохранение записей в формате XML
TOCTitle: Persisting records in XML format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 10a5651c74580950810211c4f71e19fc80a16a95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287568"
---
# <a name="persisting-records-in-xml-format"></a>Сохранение записей в формате XML

**Область применения**: Access 2013, Office 2013

Как и в формате АДТГ, сохранение **записей** в формате XML реализуется с помощью поставщика сохраняемости Microsoft OLE DB. Этот поставщик создает однонаправленный набор строк, предназначенный только для чтения, из сохраненного XML-файла или потока, который содержит сведения о схеме, созданные ADO. Аналогично, он может принимать **набор записей**ADO, создавать XML и сохранять его в файл или любой объект, реализующий интерфейс COM **IStream** . (Фактически, файл — это просто другой пример объекта, который поддерживает интерфейс **IStream**.) Для версий 2,5 и более поздних, ADO использует средство синтаксического анализа Microsoft XML (MSXML) для загрузки XML-кода в **набор записей**; Поэтому необходимо указать MSXML. dll. Для версии 2,5 MSXML поставляется с Internet Explorer 5. Для версии 2,6 MSXML поставляется с SQL Server 2000.

> [!NOTE]
> При сохранении иерархических **наборов записей** (форм данных) в формате XML применяются некоторые ограничения. Сохранение в XML невозможно, если иерархический **набор записей** содержит ожидающие обновления, и вы не можете сохранить параметризованный иерархический **набор записей**. Более подробную информацию можно узнать [в статье иерархиЧеские наборы записей в XML](hierarchical-recordsets-in-xml.md).


Самый простой способ сохранить данные в XML и повторно загрузить их через ADO с помощью методов **Save** и **Open** соответственно. В приведенном ниже примере кода ADO показано, как сохранить данные из таблицы titles в файл с именем Titles. САВ.

```vb 
 
Dim rs as new Recordset 
Dim rs2 as new Recordset 
Dim c as new Connection 
Dim s as new Stream 
 
' Query the Titles table. 
c.Open "provider='sqloledb';data source='mydb';initial catalog='pubs';Integrated Security='SSPI'" 
rs.cursorlocation = adUseClient 
rs.Open "select * from titles", c, adOpenStatic 
 
' Save to the file in the XML format. Note that if you don't specify 
' adPersistXML, a binary format (ADTG) will be used by default. 
rs.Save "titles.sav", adPersistXML 
 
' Save the Recordset into the ADO Stream object. 
rs.save s, adPersistXML 
rs.Close 
c.Close 
 
set rs = nothing 
 
Reopen the file. 
rs.Open "titles.sav",,,,adCmdFile 
'Open the Stream back into a Recordset. 
rs2.open s 
```

ADO всегда сохраняет весь объект **Recordset** . Если требуется только хранить подмножество строк объекта **Recordset** , используйте метод **Filter** для сужения списка строк или изменения условия выбора. Тем не менее, необходимо открыть объект **Recordset** с помощью клиентского курсора (**CursorLocation** = **адусеклиент**), чтобы использовать метод **Filter** для сохранения подмножества строк. Например, чтобы получить названия, начинающиеся с буквы "b", можно применить фильтр к открытому объекту **Recordset** :

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO всегда использует набор строк обработчика клиентского курсора для создания прокручиваемого объекта **Recordset** поверх данных, созданных поставщиком сохраняемости.

В этой статье содержатся следующие разделы:

- [XML Persistence Format](xml-persistence-format.md)

- [Пространства имен](namespaces.md)

- [Schema Section](schema-section.md)

- [Data Section](data-section.md)

- [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md)

- [Recordset Dynamic Properties in XML](recordset-dynamic-properties-in-xml.md)

- [XSLT Transformations](xslt-transformations.md)

- [Saving to the XML DOM Object](saving-to-the-xml-dom-object.md)

- [XML Security Considerations](xml-security-considerations.md)

- [XML Recordset Persistence Scenario Topics](xml-recordset-persistence-scenario.md)
