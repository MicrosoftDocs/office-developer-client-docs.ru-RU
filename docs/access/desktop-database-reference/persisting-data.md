---
title: Сохраняющиеся данные (ссылка на настольные базы данных)
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

Переносные вычисления (например, с помощью ноутбуков) создали потребность в приложениях, которые могут работать как в подключенной, так и отключенной состоянии. ADO добавила поддержку для этого, дав разработчику возможность сохранить клиентский курсор **Recordset** на диске и перезагрузить его позже.

Существует несколько сценариев, в которых можно использовать этот тип функции, включая следующие:

- **Путешествия:** При принятии приложения на дороге жизненно важно предоставить возможность вносить изменения и добавлять новые записи, которые затем могут быть подключены к базе данных позже и зафиксированы.

- **Нечасто обновляются просмотры:** Часто в приложении таблицы используются в качестве lookups ( например, таблицы налога на состояние). Они нечасто обновляются и только для чтения. Вместо того, чтобы перечитывать эти данные с сервера каждый раз, когда приложение запущено, приложение может просто загрузить данные из локально сохраняемого **Набор записей**.

В ADO для сохранения и загрузки наборов записей используйте методы **Recordset.Save** и **Recordset.Open (,,,,adCmdFile)** для объекта ADO  **Recordset.**

Вы можете использовать метод **Recordset** **Save,** чтобы сохранить набор записей **ADO** в файле на диске. (Вы также можете сохранить **набор записей для** объекта ADO **Stream.** **Объекты** потока обсуждаются позже в руководстве.) Позже можно использовать метод **Open** для повторного открытия **наборов записей,** когда вы будете готовы к его использованию. По умолчанию ADO сохраняет набор **записей** в несвободном формате Microsoft Advanced Data TableGram (ADTG). Этот двоичный формат определяется с помощью **значения adPersistADTG** **PersistFormatEnum.** Кроме того, вы можете сохранить набор **записей** в качестве XML вместо **использования adPersistXML.** Дополнительные сведения о сохранении записей в виде XML см. в рублях "Сохранение записей [в формате XML".](persisting-records-in-xml-format.md)

Синтаксис метода **Сохранить** следующим образом:

`recordset.Save Destination, PersistFormat`

При первом сохранения **наборов записей** необязательно указывать *назначение.* Если упустить *назначение,* будет создан новый файл с именем, за набором имени к значению свойства [Source](source-property-ado-recordset.md) **в Recordset.**

Omit *Destination,* когда вы впоследствии вызываете **Сохранить** после первого сохранения или ошибки времени запуска произойдет. Если впоследствии вы вызываете **Сохранить** с помощью нового *назначения,* **набор записей** сохраняется в новом пункте назначения. Однако новое назначение и исходное назначение будут открыты.

**Сохранение** не закрывает **набор записей** или *назначения,* поэтому вы можете продолжить работу с **набором записей** и сохранить последние изменения. *Пункт назначения* остается открытым до закрытия **Набор записей,** в течение которого другие приложения могут читать, но не писать в *Пункт назначения.*

По соображениям безопасности метод **Save** позволяет использовать только низкие и настраиваемые параметры безопасности из сценария, выполненного Microsoft Internet Explorer. Дополнительные сведения о проблемах безопасности см. в статье "Проблемы безопасности ADO и RDS в Microsoft Internet Explorer" в статье ActiveX Объекты данных (ADO) в технических статьях Microsoft Data Access.

Если метод **Сохранить** вызван, пока выполняется асинхронная операция по извлечению, выполнению или обновлению, сохраните ожидание завершения асинхронной операции.  

Записи сохраняются начиная с первого ряда **наборов записей.** По **завершению** метода Сохранить текущая позиция строки перемещается в первую строку **наборов Записей.**

Для наилучших результатов задайте [свойство CursorLocation](cursorlocation-property-ado.md) **adUseClient** с **сохранением**. Если поставщик не поддерживает все функции, необходимые для сохранения объектов **Recordset,** служба Cursor предоставит эти функции.

При **сохраняемом** наборе записей с свойством **CursorLocation,** задаваемом **adUseServer,** возможности обновления **для набора записей** ограничены. Как правило, допускаются только одностоловые обновления, вставки и удаления (зависящие от функциональности поставщика). Метод [Resync](resync-method-ado.md) также недоступен в этой конфигурации.

Так как *параметр Destination* может принимать любой объект, который поддерживает интерфейс **IStream** OLE DB, можно сохранить набор **Записей** непосредственно к объекту asP **Response.**

В следующем примере методы **Сохранить** и **Открыть** используются для сохранения **наборов Записей** и их повторного открытия.

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
