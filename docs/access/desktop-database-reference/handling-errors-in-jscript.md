---
title: Handling Errors in JScript
TOCTitle: Handling Errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2a2fadb9f7f377782ce7cc7d45820769927b4f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481895"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="cd442-102">Handling Errors in JScript</span><span class="sxs-lookup"><span data-stu-id="cd442-102">Handling Errors in JScript</span></span>


<span data-ttu-id="cd442-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd442-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cd442-104">Код Microsoft JScript необходимо проверить свойство **Count** семейства **Errors** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="cd442-104">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection.</span></span> <span data-ttu-id="cd442-105">Если значение больше 0, пройдите по коллекции и печати значений, как и в любом другом языке.</span><span class="sxs-lookup"><span data-stu-id="cd442-105">If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling Example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling Example (JScript)</h1> 
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

