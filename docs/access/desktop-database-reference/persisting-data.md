---
title: Сохранение данных (Справочник по для настольных баз данных Access)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d72ba6d895fc5aac2612eb3f81ecc95ac032d49
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946750"
---
# <a name="persisting-data"></a>Сохранение данных


**Применимо к**: Access 2013, Office 2013

Портативные компьютеры (например, с помощью ноутбуков) создала потребность в приложениях, которые могут работать в подключенных и отключенных состояний. ADO добавил поддерживает это, предоставляя ее разработчик возможность сохранения курсор клиента **записей** на диск и перезагрузить его позже.

Существует несколько сценариев, в которых можно использовать этот тип функции, в том числе следующие:

- **Дороге:** При извлечении приложения в дорогу, крайне важно для предоставления возможности внести изменения и добавления новых записей, которые затем можно использовать подключение к базе данных более поздней версии и фиксации.

- **Редко обновляются операции поиска:** Зачастую в приложении, таблиц используются в качестве операции поиска —, например состояний таблиц налога. Они редко обновляются и доступны только для чтения. Вместо повторного чтения этих данных с сервера каждый раз при запуске приложения, приложение может просто загрузить данные из локально сохраненного **набора записей**.

В ADO сохранить и загрузить **наборы записей**, используйте методы **Recordset.Save** и **Recordset.Open(,,,adCmdFile)** на объект ADO **Recordset** .

Метод **Save** **записей** можно использовать для хранения набора **записей** ADO в файл на диске. (Можно также сохранить **записей** на объект ADO **потока** . Объекты **потока** рассматриваются далее в руководстве.) Более поздних версий можно использовать метод **Open** и снова откройте **записей** , когда вы готовы к его использования. По умолчанию ADO сохраняет **записей** в собственный формат TableGram дополнительные данные (ADTG). В этом двоичном формате задается с помощью **adPersistADTG** **PersistFormatEnum** значение. Кроме того можно сохранить набора **записей** в работе в формате XML вместо использования **adPersistXML**. Дополнительные сведения о сохранении наборов записей в формате XML можно [Сохранение записей в формате XML](persisting-records-in-xml-format.md).

Синтаксис метода **Save** выглядит следующим образом:

`recordset.Save Destination, PersistFormat`

При первом сохранении **набора записей**, он не является обязательным для указания *назначения*. Если параметр *результат*не задан, будет создан новый файл с именем, задайте значение свойства [источника](source-property-ado-recordset.md) **записей**.

Параметр *результат* не задан, при последовательном вызове **Сохранить** после первого сохранить или произойдет ошибка во время выполнения. При последующем вызове **Сохранить** с нового *назначения*, **записей** сохраняется в новое место назначения. Тем не менее новые назначения и конечный оба будет открыть.

**Сохранить** не закрывается **записей** или *назначения*, поэтому можно продолжать работать с **набора записей** и сохраните изменения. *Конечный* открыта, пока **записей** работает, во время которых время другие приложения для чтения, но не запись в *место назначения*.

По соображениям безопасности метод **Save** разрешает использование безопасности низкой и пользовательские параметры из сценарий, выполняемый с Microsoft Internet Explorer. Более подробное описание проблемы безопасности в разделе «ADO и RDS безопасности проблемы в Microsoft Internet Explorer» в разделе ActiveX Data Objects (ADO) технические статьи в технические статьи доступа к данным Microsoft.

Если метод **Save** вызывается при асинхронное извлечение **записей** , execute или обновить операция находится в стадии разработки, **Сохраните** блокировок до завершения асинхронной операции.

Записи сохраняются, начиная с первой строки текущего **набора записей**. После завершения метода **Save** первой строки текущего **набора записей**перемещаются текущей позиции строки.

Для достижения наилучших результатов присвойте свойству [CursorLocation](cursorlocation-property-ado.md) значение **adUseClient** с **Сохранить**. Если ваш поставщик поддерживает все функциональные возможности, необходимые для сохранения **записей** объекты, службы курсора будет предоставлять функциональные возможности.

После сохранения **записей** со свойством **CursorLocation** , задайте значение **adUseServer**ограничено возможность обновления для **набора записей** . Как правило только для одной таблицы обновления, вставки и удаления могут (в зависимости от функциональности поставщика). Метод [выполнить повторную синхронизацию](resync-method-ado.md) также недоступен в этой конфигурации.

Так как параметр *назначения* может принимать любой объект, который поддерживает интерфейс OLE DB **IStream** , можно сохранить **записей** непосредственно к объекту ASP **ответа** .

В следующем примере методы **сохранения** и **открытия** используются для сохранения **записей** и более поздних версий ее снова:

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

В этом разделе содержатся следующие разделы:

- [Дополнительные сведения о сохранения наборов записей](more-about-recordset-persistence.md)

- [Сохранение отфильтрованных и иерархических наборов записей](persisting-filtered-and-hierarchical-recordsets.md)

- [Persisting Records in XML Format (ADO)](persisting-records-in-xml-format.md)