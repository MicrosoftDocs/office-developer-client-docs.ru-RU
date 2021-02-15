---
title: Свойство Recordset.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: 8632f5fb-6e5d-5a3e-1bd7-81e1270e9531
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196807(v=office.15)
ms:contentKeyID: 48546079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 369ff9192bb592c96e17920c9771c10b70dc233b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300597"
---
# <a name="recordsetcachesize-property-dao"></a>Свойство Recordset.CacheSize (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально. Для чтения и записи, **Long**.

## <a name="syntax"></a>Синтаксис

*выражение .* CacheSize

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Значение свойства **CacheSize** должно быть от 5 до 1200, но не больше, чем позволяет доступная память. Обычно используется значение 100. Если параметр имеет 0, кэшинг отключается.

Кэшинг данных повышает производительность при использовании объектов **Recordset** для извлечения данных с удаленного сервера. Кэш — это пространство в локальной памяти, в которое вмещаются данные, полученные с сервера; Это полезно, если пользователи запрашивают данные еще раз во время работы приложения. Когда пользователи запрашивают данные, ячеек базы данных Microsoft Access сначала проверяет кэш на наличие запрашиваемой информации, а не запрашивает их с сервера, что занимает больше времени. Кэш сохраняет только данные, полученные из источника данных ODBC.

Любой источник данных ODBC, подключенный к ячею базы данных Microsoft Access, например связанная таблица, может иметь локальный кэш. Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, установите свойства **CacheSize** и **[CacheStart,](recordset-cachestart-property-dao.md)** а затем используйте метод **[FillCache](recordset-fillcache-method-dao.md)** или пошаговую обработку записей с помощью методов **Move.**

Параметр свойства **CacheSize** можно создать на основе количества записей, которые приложение может обрабатывать одновременно. Например, если в качестве источника данных, отображаемого на экране, используется объект **Recordset,** можно установить для свойства **CacheSize** 20 одновременное отображение 20 записей.

Механизм баз данных Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.

Записи, полученные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.

Чтобы принудительно обновить все кэшные данные, установите для свойства **CacheSize** объекта **Recordset** 0, повторно установите для него размер кэша, который вы изначально запросили, а затем используйте метод **FillCache.**

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
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
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
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
