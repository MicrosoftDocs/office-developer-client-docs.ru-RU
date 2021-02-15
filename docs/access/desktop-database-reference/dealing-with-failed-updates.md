---
title: Исправление неудачных обновлений
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9a44548fd8747428b12c03c24207f36d3871e349
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294164"
---
# <a name="dealing-with-failed-updates"></a>Исправление неудачных обновлений

**Область применения**: Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Dealing with Failed Updates

Когда обновление завершается ошибками, то то, как устранить ошибки, зависит от характера и серьезности ошибок и логики приложения. Однако если база данных совместно используется другими пользователями, обычно ошибка в том, что кто-то другой изменяет поле до того, как это сделать. Этот тип ошибки называется *конфликтом.* ADO обнаруживает эту ситуацию и сообщает об ошибке.

Если имеются ошибки обновления, они будут захвачены в процедуру обработки ошибок. **Отфильтруем набор** записей с помощью константы **adFilterConflictingRecords,** чтобы были видны только конфликтующие строки. В этом примере стратегия разрешения ошибок заключается только в печати первых и последних имен автора (**au \_ fname** и **au \_ lname).**

Код оповещения пользователя о конфликте обновлений выглядит так:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

