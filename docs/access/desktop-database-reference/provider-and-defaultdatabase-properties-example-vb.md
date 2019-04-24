---
title: Пример использования свойств Provider и DefaultDatabase (VB)
TOCTitle: Provider and DefaultDatabase properties example (VB)
ms:assetid: 337b90e6-851d-2101-0671-50c4173aec13
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249104(v=office.15)
ms:contentKeyID: 48544107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 81c0a12a84f948fff483f236052c01eeeeb88d0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301164"
---
# <a name="provider-and-defaultdatabase-properties-example-vb"></a><span data-ttu-id="307f9-102">Пример использования свойств Provider и DefaultDatabase (VB)</span><span class="sxs-lookup"><span data-stu-id="307f9-102">Provider and DefaultDatabase properties example (VB)</span></span>


<span data-ttu-id="307f9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="307f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="307f9-104">В этом примере показано свойство [provider](provider-property-ado.md) , открывающее три объекта [подключения](connection-object-ado.md) с использованием разных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="307f9-104">This example demonstrates the [Provider](provider-property-ado.md) property by opening three [Connection](connection-object-ado.md) objects using different providers.</span></span> <span data-ttu-id="307f9-105">Кроме того, свойство [DefaultDatabase](defaultdatabase-property-ado.md) используется для задания базы данных по умолчанию для поставщика Microsoft ODBC.</span><span class="sxs-lookup"><span data-stu-id="307f9-105">It also uses the [DefaultDatabase](defaultdatabase-property-ado.md) property to set the default database for the Microsoft ODBC Provider.</span></span>

```vb 
 
'BeginProviderVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection strings 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim Cnxn3 As ADODB.Connection 
 Dim strCnxn As String 
 
 ' Open a connection using the Microsoft ODBC provider 
 Set Cnxn1 = New ADODB.Connection 
 Cnxn1.ConnectionString = "driver={SQL Server};server='MySqlServer';" & _ 
 "user id='MyUserID';password='MyPassword';" 
 Cnxn1.Open strCnxn 
 Cnxn1.DefaultDatabase = "Pubs" 
 
 ' Display the provider 
 MsgBox "Cnxn1 provider: " & Cnxn1.Provider 
 
 ' Open a connection using the Microsoft Jet provider 
 Set Cnxn2 = New ADODB.Connection 
 Cnxn2.Provider = "Microsoft.Jet.OLEDB.4.0" 
 Cnxn2.Open "C:\Program Files\Microsoft Office\Office\Samples\northwind.mdb", _ 
 "MyUserID", "MyPassword" 
 
 ' Display the provider. 
 MsgBox "Cnxn2 provider: " & Cnxn2.Provider 
 
 ' Open a connection using the Microsoft SQL Server provider 
 Set Cnxn3 = New ADODB.Connection 
 Cnxn3.Provider = "sqloledb" 
 Cnxn3.Open "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 ' Display the provider 
 MsgBox "Cnxn3 provider: " & Cnxn3.Provider 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Cnxn3.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Set Cnxn3 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Not Cnxn3 Is Nothing Then 
 If Cnxn3.State = adStateOpen Then Cnxn3.Close 
 End If 
 Set Cnxn3 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndProviderVB 
```

