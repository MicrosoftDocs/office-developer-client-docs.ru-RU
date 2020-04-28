---
title: Метод Recordset.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300520"
---
# <a name="recordsetfillcache-method-dao"></a>Метод Recordset.FillCache (DAO)

**Область применения**: Access 2013, Office 2013

Заполняет полностью или частично локальный кэш для объекта **Recordset**, который содержит данные из источника ODBC, подключенного к ядру СУБД Microsoft Access (только для баз данных ODBC, подключенных к Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . FillCache (***строки***, ***стартбукмарк***)

*expression*: переменная, представляющая объект **Recordset**.

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
<td><p><strong>Variant</strong> (подтип<strong>целого числа</strong> ), который указывает количество строк для хранения в кэше. Если опустить этот аргумент, значение определяется значением свойства <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (подтип<strong>String</strong> ), задающий закладку. Заполнение кэша начинается с записи, указанной этой закладкой. Если опустить этот аргумент, выполняется заполнение кэша, начиная с записи, указанной свойством <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Кэширование повышает производительность приложения, которое получает данные с удаленного сервера. Кэш — это пространство в локальной памяти, в котором хранятся данные, которые были получены последними с сервера; Предполагается, что данные, скорее всего, будут повторно запрошены во время выполнения приложения. Когда пользователь запрашивает данные, ядро СУБД Microsoft Access сначала проверяет кэш данных, а не извлекает его с сервера, что занимает больше времени. Кэш не сохраняет данные, которые не поступают из источника данных ODBC.

Вместо того чтобы ожидать заполнения кэша записями, можно использовать метод **FillCache** , чтобы явным образом заполнить кэш в любой момент. Это более быстрый способ заполнения кэша, так как **FillCache** получает сразу несколько записей, а не по одному. Например, когда вы просматриваете каждую запись с экрана, приложение использует **FillCache** для получения следующего экрана записей для просмотра.

Любой источник данных ODBC, подключенный к ядру СУБД Microsoft Access, доступ к которому осуществляется с помощью объектов **Recordset** , может иметь локальный кэш. Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, а затем задайте свойства **CacheSize** и **CacheStart** для объекта **Recordset**.

Если строки и стартбукмарк создают диапазон записей, частично или полностью вне диапазона записей, указанных в свойствах **CacheSize** и **CacheStart** , часть набора записей за пределами этого диапазона игнорируется и не будет загружаться в кэш.

Если **FillCache** запрашивает больше записей, чем число, оставшееся в удаленном источнике данных, ядро СУБД Microsoft Access извлекает только оставшиеся записи, и ошибка не возникнет.

> [!NOTE]
> - Записи, извлеченные из кэша, не отражают параллельные изменения, внесенные другими пользователями в исходные данные.
> - **FillCache** извлекает только те записи, которые еще не были кэшированы. Чтобы принудительно обновить все кэшированные данные, присвойте свойству **CacheSize** объекта **Recordset** значение 0, сбросьте его до размера кэша, который вы изначально запросили, а затем используйте **FillCache**.

## <a name="example"></a>Пример

В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза. Затем выполняется перечисление дважды с кэшем в 50 записей. Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset 
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
