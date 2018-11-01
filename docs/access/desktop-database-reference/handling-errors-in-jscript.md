---
title: Обработка ошибок в JScript
TOCTitle: Handling Errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bb2d1e390803b22bcda84fbe2e139e3e66645626
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886601"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="7aaf7-102">Обработка ошибок в JScript</span><span class="sxs-lookup"><span data-stu-id="7aaf7-102">Handling Errors in JScript</span></span>


<span data-ttu-id="7aaf7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7aaf7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7aaf7-104">Код Microsoft JScript необходимо проверить свойство **Count** семейства **Errors** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="7aaf7-104">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection.</span></span> <span data-ttu-id="7aaf7-105">Если значение больше 0, пройдите по коллекции и печати значений, как и в любом другом языке.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-105">If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

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

