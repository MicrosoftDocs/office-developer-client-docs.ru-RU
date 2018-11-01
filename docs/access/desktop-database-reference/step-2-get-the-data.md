---
title: Этап 2. Загрузка данных
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb206d003f0f5dc6714f00c54368e493856eed1f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872251"
---
# <a name="step-2-get-the-data"></a>Этап 2. Загрузка данных


**Применимо к**: Access 2013, Office 2013

## <a name="step-2-get-the-data"></a>Этап 2. Загрузка данных

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

### <a name="next-step"></a>Дальнейшие действия

[Этап 3. Отправка данных](step-3-send-the-data.md)

