---
title: Recordset2.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: d8d195cc-6696-0583-31eb-b9988f8b7c6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835090(v=office.15)
ms:contentKeyID: 48548042
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052927
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f314644d54c7a6361cf196f4e3c2a59df8af271d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872244"
---
# <a name="recordset2cachesize-property-dao"></a>Recordset2.CacheSize Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально. Чтение и запись **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . CacheSize

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Значение свойства **CacheSize** должен быть между 5 и 1200, но не больше, чем объем доступной памяти будет разрешено. Стандартное значение равно 100. Значение 0 отключает кэширование.

Кэширование данных улучшает производительность при использовании **набора записей** объектов для извлечения данных из удаленного сервера. Кэш — это должен быть пробел в локальной памяти, в которой содержатся данные, недавно извлеченные с сервера. Это полезно, если пользователи запрашивать данные еще раз во время выполнения приложения. Когда пользователь запрашивает данные, ядро базы данных Microsoft Access кэша для запрошенные данные сначала проверяет вместо извлечение из сервера, который занимает больше времени. Кэш сохраняет только данные, поступающие из источника данных ODBC.

Любой Microsoft Access базы данных подключением модуль ODBC источник данных, например связанной таблицы может иметь локального кэша. Создание кэша, откройте объект **набора записей** из к удаленному источнику данных, задать свойства **CacheSize** и **[CacheStart](recordset2-cachestart-property-dao.md)** и затем используйте метод **[FillCache](recordset2-fillcache-method-dao.md)** или пошаговое выполнение записи с помощью методов **перемещения** .

Настройка свойства **CacheSize** можно создать на количество записей, приложение может обрабатывать за один раз. Например при использовании объекта **набора записей** как источник данных для отображения на экране может установите его свойство **CacheSize** 20 для отображения 20 записей одновременно.

Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.

Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.

Чтобы принудительно выполнить обновление всех кэшированных данных, значение 0, снова задайте для него значение размера кэша, изначально запрошен, а затем использовать метод **FillCache** свойство **CacheSize** объекта **набора записей** .

## <a name="example"></a>Пример

В этом примере используется **CacheSize**, **CacheStart** и **SourceTableName** свойства и методы **CreateTableDef** и **FillCache** дважды перечисление записей в связанной таблице. Затем выполняется перечисление записей дважды с 50 записи кэша. Затем отображается статистика производительности без кэш-памяти и кэшированные просматривает связанную таблицу.

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
