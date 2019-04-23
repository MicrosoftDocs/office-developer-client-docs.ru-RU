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
# <a name="adding-multiple-fields"></a>Добавление нескольких полей

**Область применения**: Access 2013, Office 2013

Иногда более эффективно передавать массив полей и соответствующие значения в метод **AddNew** , а не устанавливать **значение** несколько раз для каждого нового поля. Если *фиелдлист* является массивом, то *значения* также должны быть массивом с одинаковым количеством элементов; в противном случае возникает ошибка. Порядок имен полей должен быть соответствующим порядку значений полей в каждом массиве. В приведенном ниже коде в метод **AddNew** передается массив полей и массив значений.

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

