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
ms.openlocfilehash: d83fea9f8c4e464c0df5f783ca2ab29a8a8e588b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926341"
---
# <a name="recordset2fillcache-method-dao"></a>Метод Recordset2.FillCache (DAO)


**Применимо к**: Access 2013, Office 2013

Заполняет все или часть из локального кэша для объекта **набора записей** , который содержит данные из Microsoft Access базы данных подключен модуль ODBC источника данных (Microsoft Access базы данных подключен модуль ODBC только баз данных).

## <a name="syntax"></a>Синтаксис

*выражение* . FillCache (***строк***, ***StartBookmark***)

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Строки</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>Integer</strong> подтип), указывающее число строк для хранения в кэше. Если опустить аргумент значение определяется значение свойства <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p>StartBookmark</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип), указывающее закладку. Наполнения кэша, начиная с записи, указанный в параметре эту закладку. Если опустить аргумент наполнения кэша начиная с записи, указанный в параметре свойство <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Кэширование повышает производительность приложения, которое получает данные с удаленного сервера. Кэш — это место в локальной памяти, в которой содержатся данные, недавно извлеченные с сервера. предполагается, что данные, вероятно, запрашивается еще раз во время выполнения приложения. Когда пользователь запрашивает данные, ядро базы данных Microsoft Access кэша для данных сначала проверяет вместо извлечение из сервера, который занимает больше времени. Кэш не сохраняет данные, которые не поступают из источника данных ODBC.

Без необходимости кэша следует реализовать с записями, как их загрузки, можно использовать метод **FillCache** для явно заполнения кэша в любое время. Это более быстрый способ заполнения кэша, так как **FillCache** извлекает несколько записей вместо того, по одному. К примеру во время просмотра каждого один экран записей приложение использует **FillCache** для получения следующей экранной записи для просмотра.

Microsoft Access базы данных engine подключенных источников данных ODBC, доступ с помощью объектов **наборов записей** может иметь локального кэша. Чтобы создать кэш, откройте объект **набора записей** из к удаленному источнику данных и задайте его свойства **CacheSize** и **CacheStart** **набора записей**.

Если строк и startbookmark создать диапазон записей, частично или полностью вне диапазона записей, указанное в свойствах **CacheSize** и **CacheStart** , часть записей за пределами этого диапазона игнорируется и не удается загрузить в кэш.

Если **FillCache** запрашивает записей больше, чем номер, оставшихся в к удаленному источнику данных, ядро базы данных Microsoft Access извлекаются только оставшихся записей и ошибка не происходит.


> [!NOTE]
> <UL>
> <LI>
> <P>Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</P>
> <LI>
> <P><STRONG>FillCache</STRONG> только извлекает записи еще не кэшируются. Чтобы принудительно выполнить обновление всех кэшированных данных, присвойте свойству <STRONG>CacheSize</STRONG> <STRONG>записей</STRONG> значение 0, сбросить его размер кэша, который изначально запрошен и затем с помощью <STRONG>FillCache</STRONG>.</P></LI></UL>



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
