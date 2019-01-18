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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714726"
---
# <a name="persisting-records-in-xml-format"></a>Сохранение записей в формате XML

**Применимо к**: Access 2013, Office 2013

Как формат ADTG поставщик Microsoft OLE DB сохраняемость реализована хранение **записей** в формате XML. Этот поставщик создает набор строк только вперед, только для чтения из сохраненного XML-файла или потока, который содержит сведения о схеме, созданных функцией ADO. Аналогично его занять набора **записей**ADO, создать XML- и сохраните его в виде файла или любой объект, реализующий интерфейс COM **IStream** . (На самом деле файл является любой другой пример объекта, который поддерживает **IStream**.) Для версии 2.5 и более поздних версий ADO полагается на средство синтаксического анализа Microsoft XML (MSXML) для загрузки XML-кода в **набор записей**; Поэтому msxml.dll не требуется. Для версии 2.5 MSXML в состав Internet Explorer 5. Для версии 2,6 MSXML поставляется с SQL Server 2000.

> [!NOTE]
> Некоторые ограничения при сохранении иерархические **наборы записей** (данные фигуры) в формате XML. Не удается сохранить XML, если иерархических **записей** содержит ожидающие обновления и не могут сохранять параметризованный иерархических **набора записей**. Для получения дополнительных сведений см [Иерархические наборы записей в формате XML](hierarchical-recordsets-in-xml.md).


Это самый простой способ сохранения данных в формат XML и загрузить его обратно еще раз через ADO — с помощью методов **Сохранить** и **Открыть** соответственно. В следующем примере кода ADO демонстрируется сохранение данных в таблице заголовки в файл с именем titles.sav.

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

ADO всегда сохраняется весь объект **набора записей** . Если вы хотите сохраняться только подмножество строк объекта **набора записей** , используйте метод **фильтра** сузить строки или измените предложение вашего выбора. Тем не менее, необходимо открыть объект **набора записей** с курсором со стороны клиента (**CursorLocation** = **adUseClient**) использовать метод **фильтра** для сохранения подмножество строк. К примеру для получения заголовков, которые начинаются с буквы «б», можно применить фильтр open объект **набора записей** :

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO всегда использует набор строк механизм курсор клиента для создания прокручиваемой, bookmarkable объекта **набора записей** на основе данных последовательного доступа, создаваемых поставщика службы сохранения.

В этом разделе содержатся следующие разделы:

- [Формат сохранения XML](xml-persistence-format.md)

- [Пространства имен](namespaces.md)

- [Раздел схемы](schema-section.md)

- [Раздел данных](data-section.md)

- [Иерархические наборы записей в XML](hierarchical-recordsets-in-xml.md)

- [Свойства динамической записей в формате XML](recordset-dynamic-properties-in-xml.md)

- [Преобразования XSLT](xslt-transformations.md)

- [Сохранение в объектной модели DOM XML](saving-to-the-xml-dom-object.md)

- [Вопросы безопасности XML](xml-security-considerations.md)

- [XML Recordset Persistence Scenario Topics](xml-recordset-persistence-scenario.md)
