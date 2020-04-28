---
title: Использование закладок (Справочник по базам данных Access на компьютере)
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

Часто бывает полезно вернуться к определенной записи после перемещения в **наборе записей** , не прокручивать все записи и сравнивать значения. Например, при попытке поиска записи с помощью метода **Find** , если поиск не возвращает ни одной записи, он автоматически размещаются в любом конце **набора записей**. Если поставщик поддерживает их, можно использовать закладки, чтобы отметить место перед использованием метода **Find** , чтобы вы могли вернуться к Вашему расположению. Закладка — это значение типа **Variant** , однозначно идентифицирующее запись в объекте **Recordset** .

Вы также можете использовать массив вариантов закладок с методом **фильтра** **Recordset** для фильтрации по выбранному набору записей. Подробные сведения об этом способе приведены в разделе Фильтрация результатов в разделе [Работа с наборами записей](working-with-recordsets.md)далее в этой главе.

Можно использовать свойство **Bookmark** , чтобы получить закладку для записи, или задать для текущей записи в объекте **Recordset** запись, определенную допустимой закладкой. В приведенном ниже коде используется свойство **Bookmark** для задания закладки, а затем возвращается к записи с закладкой после перехода на другие записи. Чтобы определить, поддерживает ли ваш **набор записей** закладки, **используйте метод** Supports.

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

Метод [Supports](supports-method-ado.md) Supports подробно обсуждается далее.

За исключением случаев клонированных **наборов записей**, закладки уникальны для **набора записей** , в котором они были созданы, даже если используется та же команда. Это означает, что вы не можете использовать **закладку** , полученную из одного **набора записей** , чтобы перейти к той же записи во втором **наборе записей** , открытой с помощью той же команды.

