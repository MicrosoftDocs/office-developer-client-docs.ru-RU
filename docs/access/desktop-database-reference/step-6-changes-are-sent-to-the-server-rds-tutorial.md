---
title: Этап 6. Отправка изменений на сервер (руководство по RDS)
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9f75e5215e3e3d79363ab7110f7c16bcacf3cbb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998996"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a>Шаг 6: Изменения отправляются на сервер (учебник служб удаленных рабочих СТОЛОВ)

**Применимо к**: Access 2013, Office 2013

При редактировании объекта **набора записей** (строк, которые будут добавлены, изменены или удалены) изменения можно отправить на сервер.

Поведение по умолчанию служб удаленных рабочих СТОЛОВ можно вызвать неявно с объекты ADO и поставщик удаленного взаимодействия Microsoft OLE DB. Запросы могут возвращать **наборов записей**и измененного **наборов записей** можно обновить источник данных. В этом руководстве не вызывает служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

**Часть "A"** 

Предположим, в этом случае только использовали [RDS. DataControl](datacontrol-object-rds.md) , а теперь — объект **набора записей** , связанных с **RDS. DataControl**. Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных все изменения в объект **набора записей** Если свойства [сервера](server-property-rds.md) и [подключение](connect-property-rds.md) по-прежнему.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

**Часть "B"** 

Кроме того может обновить сервер с объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) определения подключения и объект **набора записей** .

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

**Это конце обучения.**

