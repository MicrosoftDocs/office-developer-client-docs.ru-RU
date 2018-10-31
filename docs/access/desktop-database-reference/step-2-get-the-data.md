---
title: Этап 2. Загрузка данных
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80dae05dc691343b3c89ce8fd3ccfe72b776984c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860331"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="c73bb-102">Этап 2. Загрузка данных</span><span class="sxs-lookup"><span data-stu-id="c73bb-102">Step 2: Get the Data</span></span>


<span data-ttu-id="c73bb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c73bb-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="c73bb-104">Этап 2. Загрузка данных</span><span class="sxs-lookup"><span data-stu-id="c73bb-104">Step 2: Get the Data</span></span>

<span data-ttu-id="c73bb-105">На этом этапе будет написание кода для открытия набора **записей** ADO и подготовка для отправки клиенту.</span><span class="sxs-lookup"><span data-stu-id="c73bb-105">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> <span data-ttu-id="c73bb-106">Откройте файл XMLResponse.asp в текстовом редакторе, например в Блокноте и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="c73bb-106">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

<span data-ttu-id="c73bb-107">Не забудьте изменить значение параметра источника данных в параметре в strCon к имени компьютера Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c73bb-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="c73bb-108">Сохранение файла перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="c73bb-108">Keep the file open and go on to the next step.</span></span>

### <a name="next-step"></a><span data-ttu-id="c73bb-109">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c73bb-109">Next step</span></span>

[<span data-ttu-id="c73bb-110">Этап 3. Отправка данных</span><span class="sxs-lookup"><span data-stu-id="c73bb-110">Step 3: Send the Data</span></span>](step-3-send-the-data.md)

