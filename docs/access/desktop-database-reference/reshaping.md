---
title: Reshaping (Access desktop database reference)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314779"
---
# <a name="reshaping"></a>Изменение формы

**Область применения**: Access 2013, Office 2013

Набору **записей,** созданному пунктом команды фигуры, может быть назначено имя псевдонима (как правило, с ключевым словом AS).  Псевдоним фигурного **recordset** можно ссылаться в совершенно другой команде. То есть можно повторно использовать или переформаировать ранее сформированный **набор записей** в новой команде фигуры. Для поддержки этой функции ADO предоставляет свойство [Reshape Name](reshape-name-property-dynamic-ado.md).

Переохитовка имеет две основные функции. Во-первых, необходимо связать существующий **набор записей** с новым родительским **набором записей.**

## <a name="example"></a>Пример

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

Вторая функция — включить доступ без глав к существующим объектам **recordset** для детей с помощью синтаксиса. `"SHAPE <recordset reshape name>"`

> [!NOTE]
> Нельзя прикрепить столбцы к существующему набору  **Recordset,** изменить параметризованный набор записей или объекты Recordset в любом пересекаемом пункте COMPUTE или выполнить совокупные операции для любого потомка **Recordset** из переостановки **recordset.**  **Переоформленный** набор записей и новая команда фигур должны использовать один и тот же объект **[Connection.](connection-object-ado.md)


