---
title: Пример использования метода Clone (VBScript)
TOCTitle: Clone method example (VBScript)
ms:assetid: b9d49eb9-8da8-dfd2-1c59-35ac70969850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249893(v=office.15)
ms:contentKeyID: 48547357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1fc3341f4ec662c17e2a7c274b1cc3af215c877c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296334"
---
# <a name="clone-method-example-vbscript"></a><span data-ttu-id="f54f7-102">Пример использования метода Clone (VBScript)</span><span class="sxs-lookup"><span data-stu-id="f54f7-102">Clone method example (VBScript)</span></span>


<span data-ttu-id="f54f7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f54f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f54f7-104">В этом примере используется метод [Clone](clone-method-ado.md), чтобы создать копии объекта [Recordset](recordset-object-ado.md), после чего пользователь может разместить указатели записей для каждой копии независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="f54f7-104">This example uses the [Clone](clone-method-ado.md) method to create copies of a [Recordset](recordset-object-ado.md) and then lets the user position the record pointer of each copy independently.</span></span>

<span data-ttu-id="f54f7-105">Используйте следующий пример на странице Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="f54f7-105">Use the following example in an Active Server Page (ASP).</span></span> <span data-ttu-id="f54f7-106">В этом примере используется база данных Northwind, распределенная с помощью Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f54f7-106">This example uses the Northwind database distributed with Microsoft Access.</span></span> <span data-ttu-id="f54f7-107">Вырезать и ввести следующий код в Блокнот или другой текстовый редактор и сохранить его как **CloneVBS.asp**.</span><span class="sxs-lookup"><span data-stu-id="f54f7-107">Cut and paste the following code to Notepad or another text editor and save it as **CloneVBS.asp**.</span></span> <span data-ttu-id="f54f7-108">Результат можно просмотреть в любом браузере клиента.</span><span class="sxs-lookup"><span data-stu-id="f54f7-108">You can view the result in any client browser.</span></span>

<span data-ttu-id="f54f7-109">Чтобы осуществить пример, измените строку RsCustomerList.Source = "Customers" на RsCustomerList.Source = "Products" для подсчета таблицы большего размера.</span><span class="sxs-lookup"><span data-stu-id="f54f7-109">To exercise the example, change the line RsCustomerList.Source = "Customers" to to RsCustomerList.Source = "Products" to count a larger table.</span></span>

```vb 
 
<!-- BeginCloneVBS --> 
<% Language = VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Clone Method</TITLE> 
</HEAD> 
 
<BODY> 
 
<H1 align="center">ADO Clone Method</H1> 
<HR> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim rsFirst, rsLast, rsCount 
    Dim rsClone 
    Dim CloneFirst, CloneLast, CloneCount 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
    Cnxn.Open strCnxn 
         
    ' create and open Recordset using object refs 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
     
    rsCustomers.ActiveConnection = Cnxn 
    rsCustomers.CursorLocation = adUseClient 
    rsCustomers.CursorType = adOpenKeyset 
    rsCustomers.LockType = adLockOptimistic 
    rsCustomers.Source = strSQLCustomers 
    rsCustomers.Open 
 
    rsCustomers.MoveFirst 
    rsCount = rsCustomers.RecordCount 
    rsFirst = rsCustomers("CompanyName") 
    rsCustomers.MoveLast 
    rsLast = rsCustomers("CompanyName") 
 
    ' create clone 
    Set rsClone = rsCustomers.Clone 
    rsClone.MoveFirst 
    CloneCount = rsClone.RecordCount 
    CloneFirst = rsClone("CompanyName") 
    rsClone.MoveLast 
    CloneLast = rsClone("CompanyName") 
%> 
 
<!-- Display Results --> 
<H3>There Are <%=rsCount%> Records in the original recordset</H3> 
<H3>The first record is <%=rsFirst%> and the last record is <%=rsLast%></H3> 
<BR><HR> 
<H3>There Are <%=CloneCount%> Records in the original recordset</H3> 
<H3>The first record is <%=CloneFirst%> and the last record is <%=CloneLast%></H3> 
<BR><HR> 
<H4>Location of OLEDB Database</H4> 
 
<% 
    ' Show location of DSN data source 
    Response.Write(Cnxn) 
 
    ' Clean up 
    If rsCustomers.State = adStateOpen then 
       rsCustomers.Close 
    End If 
    If rsClone.State = adStateOpen then 
       rsClone.Close 
    End If 
    If Cnxn.State = adStateOpen then 
       Cnxn.Close 
    End If 
    Set rsCustomers = Nothing 
    Set rsClone = Nothing 
    Set Cnxn = Nothing 
%> 
</BODY> 
</HTML> 
<!-- EndCloneVBS --> 
 
```

