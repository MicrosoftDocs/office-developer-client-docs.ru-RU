---
title: 'Шаг 2: Получение данных'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4b93eb3e3679fdbc235f4406b0480ad2597d25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480030"
---
# <a name="step-2-get-the-data"></a>Шаг 2: Получение данных


**Применимо к**: Access 2013 | Office 2013

## <a name="step-2-get-the-data"></a>Шаг 2: Получение данных

На этом этапе будет написание кода для открытия набора **записей** ADO и подготовка для отправки клиенту. Откройте файл XMLResponse.asp в текстовом редакторе, например в Блокноте и вставьте следующий код:

```vb 
 
<%@ language="VBScript" %> 
 
<!-- #include file='adovbs.inc' --> 
 
<% 
  Dim strSQL, strCon 
  Dim adoRec  
  Dim adoCon  
  Dim xmlDoc  
 
  ' You will need to change "slqServer" below to the name of the SQL  
  ' server machine to which you want to connect. 
  strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
  Set adoCon = server.createObject("ADODB.Connection") 
  adoCon.Open strCon 
 
  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
  Set adoRec = Server.CreateObject("ADODB.Recordset") 
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
```

Не забудьте изменить значение параметра источника данных в параметре в strCon к имени компьютера Microsoft SQL Server.

Сохранение файла перейдите к следующему шагу.

**Далее** [Шаг 3: отправка данных](step-3-send-the-data.md)

