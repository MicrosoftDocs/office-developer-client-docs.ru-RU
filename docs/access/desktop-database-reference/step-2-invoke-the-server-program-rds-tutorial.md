---
title: 'Step 2: Invoke the Server Program (RDS Tutorial)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edd9f8561e6275e3b8eb33e86be745345d7c797a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482801"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a>Step 2: Invoke the Server Program (RDS Tutorial)


**Применимо к**: Access 2013 | Office 2013

При вызове метода для клиента *прокси-сервера*, самой программы на сервере выполняется метод. На этом этапе будет выполнить запрос на сервере.

**Часть "A"** Если не были [RDSServer.DataFactory](datafactory-object-rdsserver.md) в этом руководстве, самый удобный способ выполните этот шаг будет использовать [RDS. DataControl](datacontrol-object-rds.md) объекта. **RDS. DataControl** объединяет предыдущие действия по созданию прокси-сервер, с помощью этот шаг, выполнение запроса.

Установка **RDS. DataControl** объекта свойства [сервера](server-property-rds.md) для идентификации, где следует присвоить значение программы сервера; свойства [подключения](connect-property-rds.md) , чтобы указать строки подключения для доступа к источнику данных; и свойства [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) , чтобы указать текст команды запроса. Затем заключать метод [Refresh](refresh-method-rds.md) , чтобы программа server для подключения к источнику данных, извлечение строк, указанным в запросе и возвращают объект **набора записей** клиенту.

В этом руководстве не использует **RDS. DataControl**, но это, как она будет выглядеть при как:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

Ни учебника по вызов служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

**Часть "B"** Общий метод выполнения этого этапа — это для вызова метода [Query](query-method-rds.md) объекта **RDSServer.DataFactory** . Этот метод принимает строку подключения, которая используется для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемых из источника данных.

В этом руководстве использует объект **DataFactory** метод **запроса** :

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

