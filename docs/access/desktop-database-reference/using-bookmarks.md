---
title: Using Bookmarks (Access desktop database reference)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 469d8a0cc9b644fe434770d51c21d8210c8038d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306309"
---
# <a name="using-bookmarks"></a>Использование закладок


**Область применения**: Access 2013, Office 2013

Часто полезно возвращаться непосредственно к определенной записи после перемещений в **наборе recordset** без прокрутки каждой записи и сравнения значений. Например, если попытаться найти запись с помощью метода **Find,** но поиск не возвращает записей, вы автоматически помещаете в любом конце **recordset**. Если ваш поставщик поддерживает их, закладки можно использовать для пометки места перед использованием метода **Find,** чтобы вы могли вернуться в расположение. Закладка — это значение **типа Variant,** которое уникальным образом идентифицирует запись в **объекте Recordset.**

Вы также можете использовать массив вариантов закладок с методом **фильтра Recordset** **для** фильтрации по выбранному набору записей. Подробные сведения об этом методе см. [](working-with-recordsets.md)в разделе "Фильтрация результатов" далее в этой главе.

Вы можете использовать свойство **Bookmark,** чтобы получить закладку для записи, или установить текущую запись в объекте **Recordset** для записи, которая определена допустимой закладкой. Следующий код использует свойство **Bookmark** для закладки, а затем возвращается к записи с закладкой после перехода к другим записям. Чтобы определить, поддерживает **ли набор recordset** закладки, используйте метод **Supports.**

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

Метод [Supports](supports-method-ado.md) более подробно освещается позже.

За исключением клонированных наборов записей, закладки  уникальны для тех наборов записей, в которых они были созданы, даже если используется та же команда.  Это означает, что  нельзя использовать закладку, полученную из одного **recordset,** для перемещения в ту же запись во втором наборе записей, открытом с помощью той же команды. 

