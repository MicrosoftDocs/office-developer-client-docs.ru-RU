---
title: Create Method Example (VB)
TOCTitle: Create Method Example (VB)
ms:assetid: 3e6a4f3d-3b25-2dfb-5ef3-6a4c5326b78f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249171(v=office.15)
ms:contentKeyID: 48544372
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df55297ecc4ebd6875b4b28cc7bc45038789d83c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482312"
---
# <a name="create-method-example-vb"></a><span data-ttu-id="19645-102">Create Method Example (VB)</span><span class="sxs-lookup"><span data-stu-id="19645-102">Create Method Example (VB)</span></span>


<span data-ttu-id="19645-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19645-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19645-104">Следующий код демонстрирует создание новой базы данных Microsoft Jet с помощью метода [Create](create-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="19645-104">The following code shows how to create a new Microsoft Jet database with the [Create](create-method-adox.md) method.</span></span>

```vb 
 
' BeginCreateDatabseVB 
Sub CreateDatabase() 
 On Error GoTo CreateDatabaseError 
 
 Dim cat As New ADOX.Catalog 
 cat.Create "Provider='Microsoft.Jet.OLEDB.4.0';Data Source='c:\new.mdb'" 
 
 'Clean up 
 Set cat = Nothing 
 Exit Sub 
 
CreateDatabaseError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateDatabaseVB 
```

