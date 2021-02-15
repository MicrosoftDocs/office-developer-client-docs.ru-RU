---
title: Persisting data (Access desktop database reference)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f5788216a20e62cfc39fd2081f4f672bc4f9b808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287603"
---
# <a name="persisting-data"></a>Сохранение данных


**Область применения**: Access 2013, Office 2013

Переносимые вычисления (например, на ноутбуках) создали потребность в приложениях, которые могут работать как в подключенных, так и в отключенных состояниях. ADO добавила поддержку этого, предоставляя разработчику возможность сохранить  набор записей курсора клиента на диск и перезагрузить его позже.

Существует несколько сценариев, в которых можно использовать этот тип функций, в том числе следующие:

- **В пути:** При получении приложения в пути важно предоставить возможность вносить изменения и добавлять новые записи, которые затем можно будет повторно подключить к базе данных позже и зафиксировать.

- **Редко обновляются подыскаки:** Часто в приложении таблицы используются в качестве подсмотра, например таблицы налога на состояние. Они обновляются редко и являются только для чтения. Вместо того чтобы перечитать эти данные с сервера при каждом начале работы приложения, приложение может просто загрузить данные из локально сохраняемого **наборов записей.**

In ADO, to save and load **Recordsets,** use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.

С помощью метода **Recordset** **Save** можно сохранить набор записей **ADO** в файле на диске. (Вы также можете сохранить **объект Recordset** в объекте ADO **Stream.** **Объекты Stream** обсуждаются далее в руководстве.) Позже вы можете использовать метод **Open,** чтобы повторно открыть **набор записей,** когда будете готовы к его использованию. По умолчанию ADO сохраняет **набор recordset** в проприетарном формате Microsoft Advanced Data TableGram (ADTG). Этот двоичный формат указывается с помощью значения **adPersistADTG** **PersistFormatEnum.** Кроме того, вы можете сохранить набор **записей** в XML вместо **adPersistXML.** Дополнительные сведения о сохранении записей в формате XML см. в подсети [Persisting Records in XML Format.](persisting-records-in-xml-format.md)

Синтаксис метода **Save:**

`recordset.Save Destination, PersistFormat`

При первом сохранения **recordset** указывать назначение *необязательно.* Если опустить *destination,* будет создан новый файл со значением свойства [Source](source-property-ado-recordset.md) объекта **Recordset.**

Опустить *назначение при* последующем вызове **"Сохранить"** после первого сохранения или возникновения ошибки во время запуска. При последующем вызове **функции "Сохранить** с новым назначением" набор  **записей** сохраняется в новом месте назначения. Однако новое и исходное назначения будут открыты.

**Сохранение** не закрывает набор **записей** или *назначение,* поэтому вы можете продолжать работать с **набором записей** и сохранять последние изменения. *Назначение* остается открытым, пока **набор записей** не будет закрыт, в течение которого другие приложения могут читать, но не записывать данные в *destination.*

В целях безопасности метод **Save** позволяет использовать только параметры низкой и настраиваемой безопасности из сценария, выполненного Microsoft Internet Explorer. Более подробное описание проблем безопасности см. в статье "ADO and RDS Security Issues in Microsoft Internet Explorer" статьи ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.

Если метод **Save** вызван во время  выполнения операции асинхронного получения, выполнения или обновления наборов записей,  сохранение будет выполняться до завершения асинхронной операции.

Записи сохраняются, начиная с первой строки **наборов записей.** После завершения работы метода **Save** текущая позиция строки перемещается в первую строку **recordset.**

Для наилучших результатов задайте для свойства [CursorLocation](cursorlocation-property-ado.md) свойство **adUseClient** с **сохранением.** Если поставщик не поддерживает все функции, необходимые для сохранения объектов **Recordset,** служба курсоров предоставляет эту функцию.

Если набор **записей** сохраняется со свойством **CursorLocation,** установленным для **adUseServer,** возможность обновления для **набора записей** ограничена. Как правило, разрешены только обновления, вставки и удаления из одной таблицы (в зависимости от функциональности поставщика). Метод [Resync](resync-method-ado.md) также недоступен в этой конфигурации.

Так как *параметр Destination* может принимать любой объект, который поддерживает интерфейс OLE DB **IStream,** можно сохранить **объект Recordset** непосредственно в объекте ответа **ASP.**

В следующем примере методы **Save** и **Open** используются для сохранения **recordset,** а затем повторного открытия:

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

В этой статье содержатся следующие разделы:

- [More About Recordset Persistence](more-about-recordset-persistence.md)

- [Persisting Filtered and Hierarchical Recordsets](persisting-filtered-and-hierarchical-recordsets.md)

- [Persisting Records in XML Format (ADO)](persisting-records-in-xml-format.md)
