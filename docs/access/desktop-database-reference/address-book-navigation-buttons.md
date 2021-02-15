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

Приложение адресной книги отображает кнопки навигации в нижней части веб-страницы. Вы можете использовать кнопки навигации для навигации по данным в сетке HTML, выбрав первую или последнюю строку данных или строки, расположенные рядом с текущим выделением.

## <a name="navigation-sub-procedures"></a>Под процедуры навигации

Приложение адресной книги содержит несколько процедур, позволяющих пользователям нажимать  кнопки "Первый", "Далее", "Назад" и "Последний" для перемещения данных. 

Например, нажатие кнопки **"Первый"** активирует процедуру VBScript First \_ OnClick Sub. Процедура выполняет метод [MoveFirst,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) который делает первую строку данных текущим выделением. Нажатие кнопки **"Последний"** активирует процедуру Last OnClick Sub, которая вызывает метод MoveLast, делая последнюю строку данных \_ текущим выделением. [](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) Остальные кнопки навигации работают аналогично.

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

