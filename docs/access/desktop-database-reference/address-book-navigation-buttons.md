---
title: Адресной книги кнопки перехода
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1a8caae94bf56532b45dcfa3e647ba092552795
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947555"
---
# <a name="address-book-navigation-buttons"></a>Адресной книги кнопки перехода

**Применимо к**: Access 2013, Office 2013

Адресная книга приложения отображаются кнопки навигации в нижней части веб-страницы. Можно использовать кнопки перехода для перемещения по данным в отображение сетки HTML, выбрав либо первой или последней строки данных или рядом с текущего выделения строк.

## <a name="navigation-sub-procedures"></a>Процедуры Sub навигации

Приложение адресная книга содержит некоторые процедуры, которые позволяют пользователям щелкните **первый**, **Далее**, **Назад**и **последний** кнопки для перемещения данных.

Например, щелкнув **Первая** кнопка активирует первый VBScript\_процедуры OnClick Sub. Процедура выполняет метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , что делает первую строку данных текущего выделенного фрагмента. Нажатие кнопки **последней** активирует последний\_процедуры OnClick Sub, которая вызывает метод [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) текущего выделения последней строки данных. Аналогичным образом работать оставшихся кнопок навигации.

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

