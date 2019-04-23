---
title: Добавление нескольких полей
TOCTitle: Adding multiple fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bc9822f2055e7cdfd9a2ef5fe9d2312fc5622ac7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280590"
---
# <a name="adding-multiple-fields"></a><span data-ttu-id="ce037-102">Добавление нескольких полей</span><span class="sxs-lookup"><span data-stu-id="ce037-102">Adding multiple fields</span></span>

<span data-ttu-id="ce037-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce037-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce037-104">Иногда более эффективно передавать массив полей и соответствующие значения в метод **AddNew** , а не устанавливать **значение** несколько раз для каждого нового поля.</span><span class="sxs-lookup"><span data-stu-id="ce037-104">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the **AddNew** method, rather than setting **Value** multiple times for each new field.</span></span> <span data-ttu-id="ce037-105">Если *фиелдлист* является массивом, то *значения* также должны быть массивом с одинаковым количеством элементов; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ce037-105">If *FieldList* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="ce037-106">Порядок имен полей должен быть соответствующим порядку значений полей в каждом массиве.</span><span class="sxs-lookup"><span data-stu-id="ce037-106">The order of field names must match the order of field values in each array.</span></span> <span data-ttu-id="ce037-107">В приведенном ниже коде в метод **AddNew** передается массив полей и массив значений.</span><span class="sxs-lookup"><span data-stu-id="ce037-107">The following code passes an array of fields and an array of values to the **AddNew** method.</span></span>

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

