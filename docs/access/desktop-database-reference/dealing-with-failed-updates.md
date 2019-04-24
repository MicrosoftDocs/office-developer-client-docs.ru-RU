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

Когда обновление завершается с ошибками, способ устранения ошибок зависит от природы и серьезности ошибок и логики приложения. Тем не менее, если база данных используется совместно с другими пользователями, типичная ошибка заключается в том, что другой пользователь изменяет поле перед выполнением. Этот тип ошибки называется *конфликтом.* ADO обнаруживает эту ситуацию и сообщает об ошибке.

При наличии ошибок обновления они будут перехвачены в подпрограмму обработки ошибок. ОтФильтровать **набор записей** с помощью константы **адфилтерконфликтингрекордс** , чтобы отображались только конфликтующие строки. В этом примере стратегия разрешения ошибок предназначена только для того, чтобы распечатать имя и фамилию автора (**Au\_fname** и **Au\_LName**).

Код оповещения пользователя о конфликте обновления выглядит следующим образом:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

