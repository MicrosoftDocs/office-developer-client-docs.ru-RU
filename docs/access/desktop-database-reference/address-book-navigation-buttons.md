---
title: Кнопки навигации по адресной книге
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282466"
---
# <a name="address-book-navigation-buttons"></a>Кнопки навигации по адресной книге

**Область применения**: Access 2013, Office 2013

Приложение Адресная книга отображает кнопки навигации в нижней части веб-страницы. С помощью кнопок навигации можно перемещаться по данным на дисплее HTML-сетки, выбрав первый или последний ряд данных или строки, примыкающие к текущему выбору.

## <a name="navigation-sub-procedures"></a>Навигационные под процедуры

Приложение Адресная книга содержит несколько процедур, которые позволяют пользователям щелкнуть кнопки **First,** **Next,** **Previous** и **Last** для перемещения данных.

Например, щелкнув первую **кнопку,** активирует процедуру VBScript First \_ OnClick Sub. Процедура выполняет метод [MoveFirst,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) который делает первый ряд данных текущим выбором. Нажав  последнюю кнопку, активирует процедуру Last OnClick Sub, которая вызывает метод MoveLast, делая последний ряд данных \_ текущим выбором. [](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) Остальные кнопки навигации работают аналогичным образом.

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

