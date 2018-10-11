---
title: Persisting Records in XML Format
TOCTitle: Persisting Records in XML Format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b1e22c3f85c4289520326c34c6d0c218a442a3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481623"
---
# <a name="persisting-records-in-xml-format"></a>Persisting Records in XML Format


**Применимо к**: Access 2013 | Office 2013

Как формат ADTG поставщик Microsoft OLE DB сохраняемость реализована хранение **записей** в формате XML. Этот поставщик создает набор строк только вперед, только для чтения из сохраненного XML-файла или потока, который содержит сведения о схеме, созданных функцией ADO. Аналогично его занять набора **записей**ADO, создать XML- и сохраните его в виде файла или любой объект, реализующий интерфейс COM **IStream** . (На самом деле файл является любой другой пример объекта, который поддерживает **IStream**.) Для версии 2.5 и более поздних версий ADO полагается на средство синтаксического анализа Microsoft XML (MSXML) для загрузки XML-кода в **набор записей**; Поэтому msxml.dll не требуется. Для версии 2.5 MSXML в состав Internet Explorer 5. Для версии 2,6 MSXML поставляется с SQL Server 2000.


> [!NOTE]
> <P>Некоторые ограничения при сохранении иерархические <STRONG>наборы записей</STRONG> (данные фигуры) в формате XML. Не удается сохранить XML, если иерархических <STRONG>записей</STRONG> содержит ожидающие обновления и не могут сохранять параметризованный иерархических <STRONG>набора записей</STRONG>. Для получения дополнительных сведений см <A href="hierarchical-recordsets-in-xml.md">Иерархические наборы записей в формате XML</A>.</P>



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

