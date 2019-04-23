---
title: Постоянное исправление данных (Справочник по базам данных Access на компьютере)
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

Портативные компьютеры (например, с помощью ноутбуков) создавали потребность в приложениях, которые могут работать в подключенном и отключенном состояниях. ADO добавлена поддержка этой функции, предоставляя разработчикам возможность сохранить на диске **набор записей** клиентского курсора и перезагрузить его позже.

Существует несколько сценариев, в которых можно использовать этот тип функции, в том числе следующие:

- **Путешествие:** При получении приложения в дороге необходимо предоставить возможность вносить изменения и добавлять новые записи, которые затем могут быть повторно подключены к базе данных позднее и зафиксированы.

- **Нечасто обновляемые подстановки:** Часто в приложении таблицы используются в качестве подстановок — например, таблицы сведений о состоянии налога. Они редко обновляются и доступны только для чтения. Вместо повторного считывания этих данных с сервера при каждом запуске приложения приложение может просто загрузить данные из локально материализованного **набора записей**.

В ADO для сохранения и загрузки **наборов записей**используйте методы **Recordset. Save** и **Recordset. Open (,,,, адкмдфиле)** в объекте **Recordset** объекта ADO.

Можно использовать метод Save **набора записей** **** для сохранения **набора записей** ADO в файл на диске. (Вы также можете сохранить объект **Recordset** в объект **Stream** объекта ADO. Объекты **Stream** обсуждаются далее в руководстве. Позже с помощью метода **Open** можно повторно открыть **набор записей** , когда он будет готов к использованию. По умолчанию ADO сохраняет **набор записей** в собственном формате Microsoft Advanced Data ТАБЛЕГРАМ (адтг). Этот двоичный формат указывается с помощью значения **Персистформатенум** **адперсистадтг** . Кроме того, вы можете сохранить свой **набор записей** как XML-файл, а затем использовать **адперсистксмл**. Дополнительные сведения о сохранении записей в виде XML-файла приведены [в статье Сохранение записей в формате XML](persisting-records-in-xml-format.md).

Синтаксис метода **Save** выглядит следующим образом:

`recordset.Save Destination, PersistFormat`

При первом сохранении объекта **Recordset**необязательно указывать *назначение*. Если параметр *Destination*опущен, будет создан новый файл с именем, равным значению свойства [Source](source-property-ado-recordset.md) объекта **Recordset**.

При последующем вызове метода **Save** после первого сохранения или ошибки времени выполнения будет опущен *конечный объект* . Если вы затем вызываете метод **Save** с новым *пунктом назначения*, то **набор записей** сохраняется в новом месте. Тем не менее, будет открыто новое место назначения и исходное место назначения.

При **сохранении** не закрываетСя объект **Recordset** или *Destination*, поэтому вы можете продолжить работу с **набором записей** и сохранить последние изменения. *Назначение* остается открытым до закрытия **набора записей** , в то время как другие приложения могут считывать, но не записывать в *назначение*.

В целях безопасности метод **Save** позволяет использовать только нестандартные параметры безопасности из скрипта, выполняемого Microsoft Internet Explorer. Более подробное описание вопросов безопасности приведено в статьях "вопросы безопасности ADO и RDS в Microsoft Internet Explorer" в статье Data Object Data Objects (ADO Data Objects) в статье Data Data Objects (ADO) в технической статье Microsoft Data Access.

Если метод **Save** вызывается во время выполнения операции получения, выполнения или обновления в асинхронном **наборе записей** , функция **сохранения** ожидает завершения асинхронной операции.

Записи сохраняются начиная с первой строки **набора записей**. После завершения метода **Save** текущая позиция строки перемещается в первую строку **набора записей**.

Для получения лучших результатов установите для свойства [CursorLocation](cursorlocation-property-ado.md) значение **адусеклиент** с параметром **Save**. Если ваш поставщик не поддерживает все функции, необходимые для сохранения объектов **Recordset** , Служба курсора предоставит эту функцию.

Если для **** свойства **CursorLocation** задано значение **Адусесервер**, возможность обновления для **набора записей** ограничена. Как правило, допускается только обновление, вставка и удаление одной таблицы (зависит от функциональных возможностей поставщика). Метод [Resync](resync-method-ado.md) также недоступен в этой конфигурации.

Так как параметр *Destination* может принимать любой объект, поддерживающий интерфейс **IStream** OLE DB, можно сохранить объект **Recordset** непосредственно в ответном объекте **** ASP.

В следующем примере методы **Save** и **Open** используются для сохранения объекта **Recordset** , а затем повторно его открытия:

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
