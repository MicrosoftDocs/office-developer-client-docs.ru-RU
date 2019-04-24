---
title: Обработка ошибок в JScript
TOCTitle: Handling errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f06584ef752e0be7f68b3f661fbdba50b52cd20e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292043"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="4a1e7-102">Обработка ошибок в JScript</span><span class="sxs-lookup"><span data-stu-id="4a1e7-102">Handling errors in JScript</span></span>


<span data-ttu-id="4a1e7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a1e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a1e7-104">Код Microsoft JScript должен проверить свойство **Count** коллекции **ошибок** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="4a1e7-104">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection.</span></span> <span data-ttu-id="4a1e7-105">Если значение больше 0, необходимо выполнить итерацию по коллекции и напечатать значения так же, как и на любом другом языке.</span><span class="sxs-lookup"><span data-stu-id="4a1e7-105">If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling example (JScript)</h1> 
<% 
 var cnn1 = Server.CreateObject("ADODB.Connection"); 
 var errLoop = Server.CreateObject("ADODB.Error"); 
 var strError = new String; 
 
 try 
 { 
 // Intentionally trigger an error. 
 cnn1.Open("nothing"); 
 } 
 catch(e) 
 { 
 Response.Write(e.message); 
 } 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleJS --> 
```

