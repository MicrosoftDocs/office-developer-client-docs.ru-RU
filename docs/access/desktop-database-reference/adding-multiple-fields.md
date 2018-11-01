---
title: Добавление нескольких полей
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01330eeed2645a0bd76f6ac51e96542068b245e7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878978"
---
# <a name="adding-multiple-fields"></a>Добавление нескольких полей


**Применимо к**: Access 2013, Office 2013

В некоторых случаях может быть более эффективный для передачи в массиве полей и их соответствующие значения в метод **AddNew** , а не **для параметра несколько раз для каждого нового поля** . Если *FieldList* является массивом, *значения* также должны быть массив с числом участников; в противном случае возникает ошибка. Порядок имена полей должен совпадать с порядком значений полей в каждом массиве. Следующий код в метод **AddNew** передает массив полей и массив значений.

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

