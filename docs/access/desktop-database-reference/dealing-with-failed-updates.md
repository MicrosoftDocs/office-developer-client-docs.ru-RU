---
title: Работа с ошибками обновлений
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 659b5389074371ed4de41b909ab5228ad8fca080
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947751"
---
# <a name="dealing-with-failed-updates"></a>Работа с ошибками обновлений

**Применимо к**: Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Исправление неудачных обновлений

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

