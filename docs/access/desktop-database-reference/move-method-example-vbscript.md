---
title: Пример использования метода Move (VBScript)
TOCTitle: Move method example (VBScript)
ms:assetid: 42f2eb08-47cf-f422-6176-badd414d0bfc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249198(v=office.15)
ms:contentKeyID: 48544489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea9e65098637986de91b6eaf5d770f2a8cab5ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288843"
---
# <a name="move-method-example-vbscript"></a><span data-ttu-id="45150-102">Пример использования метода Move (VBScript)</span><span class="sxs-lookup"><span data-stu-id="45150-102">Move method example (VBScript)</span></span>


<span data-ttu-id="45150-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45150-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45150-104">В этом примере с помощью метода [Move](move-method-ado.md) замещается указатель записи на основании вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="45150-104">This example uses the [Move](move-method-ado.md) method to position the record pointer, based on user input.</span></span>

<span data-ttu-id="45150-105">Используйте приведенный ниже пример на активной серверной странице (ASP).</span><span class="sxs-lookup"><span data-stu-id="45150-105">Use the following example in an Active Server Page (ASP).</span></span>

<span data-ttu-id="45150-106">Используйте **Find** , чтобы найти файл адовбс. Inc и разместить его в каталоге, который планируется использовать.</span><span class="sxs-lookup"><span data-stu-id="45150-106">Use **Find** to locate the file Adovbs.inc and place it in the directory you plan to use.</span></span> <span data-ttu-id="45150-107">Скопируйте и вставьте следующий код в Блокнот или другой текстовый редактор и сохраните его как **мовевбс. ASP**.</span><span class="sxs-lookup"><span data-stu-id="45150-107">Cut and paste the following code to Notepad or another text editor, and save it as **MoveVBS.asp**.</span></span> <span data-ttu-id="45150-108">Вы можете просмотреть результат в любом браузере.</span><span class="sxs-lookup"><span data-stu-id="45150-108">You can view the result in any browser.</span></span>

<span data-ttu-id="45150-109">Попробуйте ввести букву или нецелое число, чтобы увидеть работу по обработке ошибок.</span><span class="sxs-lookup"><span data-stu-id="45150-109">Try entering a letter or noninteger to see the error handling work.</span></span>

```vb 
 
<!-- BeginMoveVBS --> 
<%@ Language=VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Move Methods</TITLE> 
<STYLE> 
<!-- 
BODY { 
   font-family: "MS SANS SERIF",sans-serif; 
    } 
.thead1 { 
   background-color: #008080;  
   font-family: 'Arial Narrow','Arial',sans-serif;  
   font-size: x-small; 
   color: white; 
   } 
.tbody {  
   text-align: center; 
   background-color: #f7efde; 
   font-family: 'Arial Narrow','Arial',sans-serif;  
   font-size: x-small; 
    } 
--> 
</STYLE> 
</HEAD> 
<BODY>  
<H3>ADO Move Methods</H3> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
 
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
 
    'Check number of user moves this session and increment by entry 
    Session("Clicks") = Session("Clicks") + Request.Form("MoveAmount") 
    Clicks = Session("Clicks") 
    ' Move to last known recordset position plus amount passed  
    rsCustomers.Move CInt(Clicks) 
 
    'Error Handling 
    If rsCustomers.EOF Then 
        Session("Clicks") = rsCustomers.RecordCount 
        Response.Write "This is the Last Record" 
        rsCustomers.MoveLast 
    ElseIf rsCustomers.BOF Then 
        Session("Clicks") = 1 
        rsCustomers.MoveFirst 
        Response.Write "This is the First Record" 
    End If 
    %> 
 
    <H3>Current Record Number is <BR> 
    <%  
    If Session("Clicks") = 0 Then Session("Clicks") = 1 
    Response.Write(Session("Clicks") )%> of <%=rsCustomers.RecordCount%></H3> 
    <HR> 
 
 
    <TABLE COLSPAN=8 CELLPADDING=5 BORDER=0> 
 
    <!-- BEGIN column header row for Customer Table--> 
 
    <TR CLASS=thead1> 
       <TD>Company Name</TD> 
       <TD>Contact Name</TD> 
       <TD>City</TD> 
    </TR> 
        <% 'display%> 
        <TR CLASS=tbody> 
          <TD> <%= rsCustomers("CompanyName")%> </TD> 
          <TD> <%= rsCustomers("ContactName")%></TD> 
          <TD> <%= rsCustomers("City")%> </TD> 
        </TR>  
    </TABLE> 
 
    <HR> 
    <Input Type=Button Name=cmdDown  Value="&lt;  "> 
    <Input Type=Button Name=cmdUp Value=" &gt;"> 
    <H5>Click Direction Arrows for Previous or Next Record 
    <BR> <BR> 
 
    <FORM Method = Post Action="MoveVbs.asp" Name=Form> 
    <TABLE> 
        <TR> 
           <TD><Input Type="Button" Name=Move Value="Move Amount "></TD> 
           <TD></TD> 
           <TD><Input Type="Text" Size="4" Name="MoveAmount" Value=0></TD> 
        <TR> 
    </TABLE> 

    Click Move Amount to use Move Method<br> 
    Enter Number of Records to Move + or - </H5>    </FORM> 
</BODY> 
 
<Script Language = "VBScript"> 
 
Sub Move_OnClick 
   ' Make sure move value entered is an integer 
   If IsNumeric(Document.Form.MoveAmount.Value)Then 
      Document.Form.MoveAmount.Value = CInt(Document.Form.MoveAmount.Value) 
      Document.Form.Submit 
   Else 
      MsgBox "You Must Enter a Number", ,"ADO-ASP Example" 
      Document.Form.MoveAmount.Value = 0 
   End If 
End Sub 
 
Sub cmdDown_OnClick 
   Document.Form.MoveAmount.Value = -1 
   Document.Form.Submit 
End Sub 
 
Sub cmdUp_OnClick 
   Document.Form.MoveAmount.Value = 1 
   Document.Form.Submit 
End Sub 
</Script> 
 
<% 
    ' clean up 
    If rsCustomers.State = adStateOpen then 
        rsCustomers.Close 
    End If 
    If Cnxn.State = adStateOpen then 
        Cnxn.Close 
    End If 
%> 
</HTML> 
<!-- EndMoveVBS --> 
```

