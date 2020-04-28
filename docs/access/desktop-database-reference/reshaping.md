---
title: Изменение формы (Справочник по базам данных Access на компьютере)
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

Для объекта **Recordset** , созданного с помощью предложения команды Shape, может быть назначен *псевдоним* (как правило, с помощью ключевого слова as). Псевдоним для объекта **Recordset** в форме может быть указан в полностью другой команде. То есть вы можете повторно использовать или *изменить форму*ранее созданного **набора записей** в новой команде Shape. Чтобы обеспечить поддержку этой функции, ADO предоставляет свойство, а также [перерисовку имени](reshape-name-property-dynamic-ado.md).

Изменение формы состоит из двух основных функций. Первый — связать существующий **набор записей** с новым родительским **набором записей**.

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

Вторая функция заключается в включении доступа, не разбитого на разделы, **Recordset** в существующие дочерние объекты `"SHAPE <recordset reshape name>"`Recordset с помощью синтаксиса.

> [!NOTE]
> Невозможно добавить столбцы к существующему **набору записей**, изменить форму параметризованного **набора записей** или объектов **Recordset** в любом промежуточном предложении COMPUTE или выполнить операции агрегирования для любого потомка **Recordset** из **набора записей** , для которого выполняется изменение формы. Объект **Recordset** , для которого выполняется изменение формы, и команда Новая фигура должна использовать один и тот же объект[подключения](connection-object-ado.md) * *.


