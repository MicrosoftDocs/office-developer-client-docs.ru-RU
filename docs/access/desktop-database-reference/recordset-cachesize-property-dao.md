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

*Expression* . CacheSize

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Значение свойства **CacheSize** должно находиться в пределах от 5 до 1200, но не больше, чем доступная память. Типичное значение — 100. Значение 0 отключает кэширование.

Кэширование данных повышает производительность, если вы используете объекты **Recordset** для получения данных с удаленного сервера. Кэш — это пространство в локальной памяти, в котором хранятся данные, которые были получены последними с сервера. Это полезно, если пользователи запрашивают данные еще раз во время выполнения приложения. Когда пользователи запрашивают данные, ядро СУБД Microsoft Access сначала проверяет кэш для запрошенных данных, а не извлекает его с сервера, что занимает больше времени. Кэш сохраняет данные, поступающие из источника данных ODBC.

Любой источник данных ODBC, подключенный к ядру СУБД Microsoft Access (например, связанная таблица), может иметь локальный кэш. Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, задайте свойства **CacheSize** и **[CacheStart](recordset-cachestart-property-dao.md)** , а затем используйте метод **[FillCache](recordset-fillcache-method-dao.md)** или Пошаговое перемещение записей с помощью методов **Move** .

Вы можете создать значение свойства **CacheSize** для количества записей, обрабатываемых приложением одновременно. Например, если вы используете объект **Recordset** в качестве источника данных, которые будут отображаться на экране, можно установить для свойства **CacheSize** значение 20, чтобы отобразить 20 записей за один раз.

Ядро СУБД Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.

Записи, извлеченные из кэша, не отражают параллельные изменения, внесенные другими пользователями в исходные данные.

Чтобы принудительно обновить все кэшированные данные, задайте для свойства **CacheSize** объекта **Recordset** значение 0, повторно задайте для него размер кэша, который вы изначально запросили, а затем используйте метод **FillCache** .

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
