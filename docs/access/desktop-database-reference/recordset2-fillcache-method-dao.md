---
title: Метод Recordset2.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2098df82375ac47b7d5abe0bd63b0af2bb29ba40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309704"
---
# <a name="recordset2fillcache-method-dao"></a>Метод Recordset2.FillCache (DAO)

**Область применения**: Access 2013, Office 2013

Заполняет полностью или частично локальный кэш для объекта **Recordset**, который содержит данные из источника ODBC, подключенного к ядру СУБД Microsoft Access (только для баз данных ODBC, подключенных к Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . FillCache ***(Строки***, ***StartBookmark***)

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Подтип <strong>Variant</strong> <strong>(Integer),</strong> который указывает количество строк для хранения в кэше. Если не упустить этот аргумент, значение определяется параметром <strong><a href="recordset2-cachesize-property-dao.md">свойства CacheSize.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Подтип</strong> <strong>Variant (String),</strong> который указывает закладки. Кэш заполняется начиная с записи, указанной этой закладкой. Если не упустить этот аргумент, кэш заполняется начиная с записи, показанной <strong><a href="recordset2-cachestart-property-dao.md">свойством CacheStart.</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Кэшинг повышает производительность приложения, которое извлекает данные с удаленного сервера. Кэш — это пространство в локальной памяти, которое содержит данные, недавно извлеченные с сервера; это предполагает, что данные, вероятно, будут запрашиваться снова во время работы приложения. Когда пользователь запрашивает данные, система базы данных Microsoft Access сначала проверяет кэш для данных, а не отбирает их с сервера, что занимает больше времени. Кэш не сохраняет данные, которые не приходят из источника данных ODBC.

Вместо ожидания заполнения кэша записями по мере их получения можно использовать метод **FillCache** для явного заполнения кэша в любое время. Это более быстрый способ заполнения кэша, так как **FillCache** извлекает сразу несколько записей вместо одной. Например, при просмотре каждой экранной записи приложение использует **FillCache** для получения следующих экранных записей для просмотра.

Любой источник данных базы данных Microsoft Access, подключенный к базе данных ODBC, к который можно получить доступ с **объектами Recordset,** может иметь локальный кэш. Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, а затем установите свойства **CacheSize** и **CacheStart** **в Наборе записей.**

Если строки и startbookmark создают диапазон записей, который частично или полностью находится за пределами диапазона записей, указанных свойствами **CacheSize** и **CacheStart,** часть наборов записей за пределами этого диапазона игнорируется и не загружается в кэш.

Если **FillCache** запрашивает больше записей, чем число, оставшееся в удаленном источнике данных, двигатель базы данных Microsoft Access извлекает только оставшиеся записи, и ошибка не возникает.

> [!NOTE]
> - Записи, извлеченные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.
> - **FillCache** только извлекает записи, которые еще не кэшировали. Чтобы принудительно обновить все кэшные данные, установите свойство **CacheSize** набора записей до 0, сбросите его до размера первоначально запрашиваемого кэша, а затем используйте **FillCache**. 

## <a name="example"></a>Пример

В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза. Затем выполняется перечисление дважды с кэшем в 50 записей. Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
       Dim sngStart As Single 
       Dim sngEnd As Single 
       Dim sngNoCache As Single 
       Dim sngCache As Single 
       Dim intLoop As Integer 
       Dim strTemp As String 
       Dim intRecords As Integer 
     
       ' Open a database to which a linked table can be  
       ' appended. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a linked table that connects to a Microsoft SQL 
       ' Server database. 
       Set tdfRoyalties = _ 
          dbsCurrent.CreateTableDef("Royalties") 
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       tdfRoyalties.Connect = _ 
          "ODBC;DATABASE=pubs;DSN=Publishers" 
       tdfRoyalties.SourceTableName = "roysched" 
       dbsCurrent.TableDefs.Append tdfRoyalties 
       Set rstRemote = _ 
          dbsCurrent.OpenRecordset("Royalties") 
     
       With rstRemote 
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          sngStart = Timer 
     
          For intLoop = 1 To 2 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                .MoveNext 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngNoCache = sngEnd - sngStart 
     
          ' Cache the first 50 records. 
          .MoveFirst 
          .CacheSize = 50 
          .FillCache 
          sngStart = Timer 
     
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          For intLoop = 1 To 2 
             intRecords = 0 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                ' Count the records. If the end of the 
                ' cache is reached, reset the cache to the 
                ' next 50 records. 
                intRecords = intRecords + 1 
                .MoveNext 
                If intRecords Mod 50 = 0 Then 
                   .CacheStart = .Bookmark 
                   .FillCache 
                End If 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngCache = sngEnd - sngStart 
     
          ' Display performance results. 
          MsgBox "Caching Performance Results:" & vbCr & _ 
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
