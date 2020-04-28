---
title: Пример использования свойства StayInSync (VB)
TOCTitle: StayInSync property example (VB)
ms:assetid: 1b35f19a-0104-efd5-5222-55f92e08473b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248952(v=office.15)
ms:contentKeyID: 48543535
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32333ab98f717e48b3411ff48b4a1f88cb107812
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314520"
---
# <a name="stayinsync-property-example-vb"></a><span data-ttu-id="85d7f-102">Пример использования свойства StayInSync (VB)</span><span class="sxs-lookup"><span data-stu-id="85d7f-102">StayInSync property example (VB)</span></span>


<span data-ttu-id="85d7f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85d7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85d7f-104">В этом примере показано, как свойство [StayInSync](stayinsync-property-ado.md) упрощает доступ к строкам в иерархическом [наборе записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="85d7f-104">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="85d7f-105">В внешнем цикле отображаются имя, состояние и идентификатор каждого автора.</span><span class="sxs-lookup"><span data-stu-id="85d7f-105">The outer loop displays each author's first and last name, state, and identification.</span></span> <span data-ttu-id="85d7f-106">Добавленный **набор записей** для каждой строки извлекается из коллекции [Fields](fields-collection-ado.md) и автоматически назначается свойству **рсттитлеаусор** **, когда** родительский объект **Recordset** перемещается в новую строку.</span><span class="sxs-lookup"><span data-stu-id="85d7f-106">The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row.</span></span> <span data-ttu-id="85d7f-107">Внутренний цикл отображает четыре поля из каждой строки добавленного набора записей.</span><span class="sxs-lookup"><span data-stu-id="85d7f-107">The inner loop displays four fields from each row in the appended recordset.</span></span>

```vb 
 
'BeginStayInSyncVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code create a DSN called Pubs 
 'with a user_id = sa and no password 
 
 Dim Cnxn As ADODB.Connection 
 Dim rst As ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 Dim strCnxn As String 
 
 ' open connection with Data Shape attributes 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider=MSDataShape;Data Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' create recordset 
 Set rst = New ADODB.Recordset 
 rst.StayInSync = True 
 rst.Open "SHAPE {select * from Authors} " & _ 
 "APPEND ( { select * from titleauthor} AS chapTitleAuthor " & _ 
 "RELATE au_id TO au_id) ", Cnxn, , , adCmdText 
 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
 Do Until rst.EOF 
 Debug.Print rst!au_fname & " " & rst!au_lname & " " & _ 
 rst!State & " " & rst!au_id 
 
 Do Until rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0) & " " & rstTitleAuthor(1) & " " & _ 
 rstTitleAuthor(2) & " " & rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Loop 
 
 rst.MoveNext 
 Loop 
 
 ' clean up 
 rst.Close 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndStayInSyncVB 
```

