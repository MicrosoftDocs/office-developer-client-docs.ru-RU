---
title: Пример использования методов Save и Open (VB)
TOCTitle: Save and Open methods example (VB)
ms:assetid: aecb56b4-3ccd-d8f1-84a9-fd5a40aeca5f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249828(v=office.15)
ms:contentKeyID: 48547081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e4eff3eae32cf4d910a44eca5a733ac044a7829
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308983"
---
# <a name="save-and-open-methods-example-vb"></a><span data-ttu-id="822df-102">Пример использования методов Save и Open (VB)</span><span class="sxs-lookup"><span data-stu-id="822df-102">Save and Open methods example (VB)</span></span>


<span data-ttu-id="822df-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="822df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="822df-104">В этих трех примерах показано, как можно использовать методы [Save](save-method-ado.md) и [Open](open-method-ado-recordset.md) вместе.</span><span class="sxs-lookup"><span data-stu-id="822df-104">These three examples demonstrate how the [Save](save-method-ado.md) and [Open](open-method-ado-recordset.md) methods can be used together.</span></span>

<span data-ttu-id="822df-105">Предположим, что вы собираетесь в бизнес-поездку и хотите взять таблицу из базы данных.</span><span class="sxs-lookup"><span data-stu-id="822df-105">Assume you are going on a business trip and want to take along a table from a database.</span></span> <span data-ttu-id="822df-106">Прежде чем перейти к данным в виде наборов [записей,](recordset-object-ado.md) сохраните их в транспортируемых формах.</span><span class="sxs-lookup"><span data-stu-id="822df-106">Before you go, you access the data as a [Recordset](recordset-object-ado.md) and save it in a transportable form.</span></span> <span data-ttu-id="822df-107">Когда вы поступаете к месту назначения, вы можете получить доступ к **набору записей** как к локальному отсоединенму **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="822df-107">When you arrive at your destination, you access the **Recordset** as a local, disconnected **Recordset**.</span></span> <span data-ttu-id="822df-108">Внося изменения в **набор записей,** сохраните его еще раз.</span><span class="sxs-lookup"><span data-stu-id="822df-108">You make changes to the **Recordset**, then save it again.</span></span> <span data-ttu-id="822df-109">Наконец, когда вы вернетесь домой, вы снова подключаетесь к базе данных и обновляете ее с помощью изменений, внесенных в пути.</span><span class="sxs-lookup"><span data-stu-id="822df-109">Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</span></span>

<span data-ttu-id="822df-110">Во-первых, получить доступ к таблице ***"Авторы"*** и сохранить ее.</span><span class="sxs-lookup"><span data-stu-id="822df-110">First, access and save the ***Authors*** table.</span></span>

```vb 
 
'BeginSaveVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstAuthors As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 Set rstAuthors = New ADODB.Recordset 
 strSQLAuthors = "SELECT au_id, au_lname, au_fname, city, phone FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenDynamic, adLockOptimistic, adCmdText 
 
 'For sake of illustration, save the Recordset to a diskette in XML format 
 rstAuthors.Save "c:\Pubs.xml", adPersistXML 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 'clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSaveVB 
```

<br/>

<span data-ttu-id="822df-111">На этом этапе вы прибыли к месту назначения.</span><span class="sxs-lookup"><span data-stu-id="822df-111">At this point, you have arrived at your destination.</span></span> <span data-ttu-id="822df-112">Вы будете получать доступ к ***таблице Authors*** как локальный, отключенный **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="822df-112">You will access the ***Authors*** table as a local, disconnected **Recordset**.</span></span> <span data-ttu-id="822df-113">Не забывайте, что для доступа к сохраненным файлам на компьютере должен быть поставщик **MSPersist,** \\Pubs.xml.</span><span class="sxs-lookup"><span data-stu-id="822df-113">Don't forget you must have the **MSPersist** provider on the machine that you are using in order to access the saved file, a:\\Pubs.xml.</span></span>

```vb 
 
'BeginSave2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rst As ADODB.Recordset 
 Set rst = New ADODB.Recordset 
 
 'For sake of illustration, we specify all parameters 
 rst.Open "c:\Pubs.xml", "Provider=MSPersist;", adOpenForwardOnly, adLockBatchOptimistic, adCmdFile 
 
 'Now you have a local, disconnected Recordset - Edit as you desired 
 '(In this example the change makes no difference) 
 rst.Find "au_lname = 'Carson'" 
 If rst.EOF Then 
 Debug.Print "Name not found." 
 Exit Sub 
 End If 
 
 rst!city = "Chicago" 
 rst.Update 
 
 'Save changes in ADTG format this time, purely for sake of illustration. 
 'Note that the previous version is still on the diskette, as a:\Pubs.xml. 
 rst.Save "c:\Pubs.adtg", adPersistADTG 
 
 ' clean up 
 rst.Close 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 'clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSave2VB 
```

<br/>

<span data-ttu-id="822df-114">Наконец, вы вернетесь домой.</span><span class="sxs-lookup"><span data-stu-id="822df-114">Finally, you return home.</span></span> <span data-ttu-id="822df-115">Теперь обновите базу данных, внося изменения.</span><span class="sxs-lookup"><span data-stu-id="822df-115">Now update the database with your changes.</span></span>

```vb 
 
'BeginSave3VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As New ADODB.Connection 
 Dim rst As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set rst = New ADODB.Recordset 
 ' The lock mode is batch optimistic because we are going to 
 ' use the UpdateBatch method. 
 rst.Open "c:\Pubs.adtg", "Provider=MSPersist;", adOpenForwardOnly, adLockBatchOptimistic, adCmdFile 
 
 ' Connect to the database, associate the Recordset with the connection 
 ' then update the database table with the changed Recordset 
 strCnxn = "Provider=SQLOLEDB;Data Source=MySqlServer;Integrated Security=SSPI;Initial Catalog=pubs;" 
 Cnxn.Open strCnxn 
 
 rst.ActiveConnection = Cnxn 
 rst.UpdateBatch 
 
 ' clean up 
 rst.Close 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 'clean up 
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
'EndSave3VB 
```

