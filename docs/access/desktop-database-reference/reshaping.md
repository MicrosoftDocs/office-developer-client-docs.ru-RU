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

Набору **записей,** созданному предложением команды фигуры, может быть назначено имя псевдонима (обычно с ключевым словом AS).  На псевдоним фигурного **recordset** можно ссылаться в совершенно другой команде. То есть вы можете повторно использовать или повторно использовать *ранее* сформированный набор **записей** в новой команде фигуры. Для поддержки этой функции ADO предоставляет свойство [Reshape Name.](reshape-name-property-dynamic-ado.md)

Решайл имеет две основные функции. Первый — это связывать существующий **набор записей** с новым родительским **набором записей.**

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

Вторая функция — включить не главный доступ к существующим объектам объекта **Recordset** с использованием синтаксиса. `"SHAPE <recordset reshape name>"`

> [!NOTE]
> Невозможно прикрепить столбцы к существующему набору  **записей,** изменить параметризованный набор записей или **объекты Recordset** в любом intervening COMPUTE-предложении или выполнить агрегатные операции с любым потомком **Recordset** из переописаемого объекта **Recordset.** The **Recordset** being reshaped and the new shape command must both use the same **[Connection](connection-object-ado.md) object.


