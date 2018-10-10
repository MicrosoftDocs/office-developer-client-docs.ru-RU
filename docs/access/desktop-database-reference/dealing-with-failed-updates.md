---
title: Dealing with Failed Updates
TOCTitle: Dealing with Failed Updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3af3026052954ec74b10026e0cf288a6aa5249
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480154"
---
# <a name="dealing-with-failed-updates"></a>Dealing with Failed Updates


**Применимо к**: Access 2013 | Office 2013

## <a name="dealing-with-failed-updates"></a>Dealing with Failed Updates

Если обновление завершается с ошибками, способ устранения ошибки зависит от природы и уровень серьезности ошибки и логики приложения. Тем не менее если база данных используется совместно с другими пользователями, типичные ошибки — это кто-либо изменяется поле перед выполнением. Этот тип ошибки называется *конфликта.* ADO обнаруживает такие ситуации и сообщает об ошибке.

При наличии ошибок обновления, они будут содержатся в обработки ошибок. Фильтрация **записей** с константой **adFilterConflictingRecords** , чтобы были видны только конфликтующие строки. В этом примере разрешение ошибок стратегия предназначена только для печати автора первого имени и фамилии (**au\_отображающее общие сведения** и **au\_lname**).

Код для предупреждения пользователя конфликт обновления выглядит следующим образом:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

