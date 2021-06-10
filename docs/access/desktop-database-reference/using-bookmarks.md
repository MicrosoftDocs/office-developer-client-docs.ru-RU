---
title: Использование закладок (ссылка на настольные базы данных)
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

Часто полезно возвращаться непосредственно к определенной записи после перемещений в **Наборе** записей без прокрутки каждой записи и сравнения значений. Например, если вы попытаетесь найти запись с помощью метода **Find,** но поиск не возвращает записи, вы автоматически помещается в любом конце **recordset**. Если поставщик поддерживает их, закладки можно использовать для маркировки вашего места перед использованием метода **Find,** чтобы вы могли вернуться в свое расположение. Закладки — это значение **типа Variant,** которое уникально идентифицирует запись в **объекте Recordset.**

Для фильтрации выбранного набора записей можно также использовать набор закладки с помощью метода **фильтра Recordset.**  Подробные сведения об этом методе см. в разделе Фильтрация результатов в разделе [Работа с записями](working-with-recordsets.md), далее в этой главе.

Вы можете использовать свойство **Bookmark** для получения закладки для записи или установить текущую запись в объекте **Recordset** к записи, идентифицированной допустимой закладкой. Следующий код использует свойство **Bookmark** для закладки, а затем возвращается к записи закладок после перехода к другим записям. Чтобы определить, поддерживает **ли ваш набор записей** закладки, используйте метод **Supports.**

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

Подробнее [о методе Supports](supports-method-ado.md) читайте позже.

За исключением клонированных наборов записей, закладки являются уникальными для **наборов записей,** в которых они были созданы, даже если используется та же команда. Это означает, что  нельзя использовать закладки, полученные из одного **recordset,** для перемещения к той же записи во втором наборе **записей,** открываемом с той же командой.

