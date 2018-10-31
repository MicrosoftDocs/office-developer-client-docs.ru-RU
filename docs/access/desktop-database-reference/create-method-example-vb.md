---
title: Пример использования метода Create (VB)
TOCTitle: Create method example (VB)
ms:assetid: 3e6a4f3d-3b25-2dfb-5ef3-6a4c5326b78f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249171(v=office.15)
ms:contentKeyID: 48544372
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3eea826ae452576e02ab6f98bd75369ff079f7de
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860065"
---
# <a name="create-method-example-vb"></a><span data-ttu-id="2f2eb-102">Пример использования метода Create (VB)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-102">Create method example (VB)</span></span>


<span data-ttu-id="2f2eb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f2eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f2eb-104">Следующий код демонстрирует создание новой базы данных Microsoft Jet с помощью метода [Create](create-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2eb-104">The following code shows how to create a new Microsoft Jet database with the [Create](create-method-adox.md) method.</span></span>

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

