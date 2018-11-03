---
title: Обработка ошибок в JScript
TOCTitle: Handling errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 886111bcb381385632cace35dd120016c63e3754
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943957"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="7ab85-102">Обработка ошибок в JScript</span><span class="sxs-lookup"><span data-stu-id="7ab85-102">Handling errors in JScript</span></span>


<span data-ttu-id="7ab85-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ab85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ab85-104">Код Microsoft JScript необходимо проверить свойство **Count** семейства **Errors** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="7ab85-104">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection.</span></span> <span data-ttu-id="7ab85-105">Если значение больше 0, пройдите по коллекции и печати значений, как и в любом другом языке.</span><span class="sxs-lookup"><span data-stu-id="7ab85-105">If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

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

