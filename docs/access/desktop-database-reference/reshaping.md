---
title: Изменения формы (доступа к рабочему столу ссылку на базу данных)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711905"
---
# <a name="reshaping"></a>Изменение формы

**Применимо к**: Access 2013, Office 2013

**Записей** , созданные с помощью предложения команду фигуры может быть назначен в имя *псевдонима* (обычно с ключевым словом AS). Псевдоним формы **записей** можно ссылаться в совершенно иной команды. То есть, который может повторно использовать, или *Изменить форму*, ранее формы **записей** в новую команду фигуры. Для поддержки этой функции, ADO предоставляет свойство, [Имя формы](reshape-name-property-dynamic-ado.md).

Изменение формы имеет две основные функции. Первый фильтр — Связывание существующих **записей** с новым родительским **набора записей**.

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

Вторая функция является возможность не разбитых доступ к существующим объектам дочерних **записей** , используя синтаксис `"SHAPE <recordset reshape name>"`.

> [!NOTE]
> Не удается добавить столбцы в существующих **записей**, изменить форму параметризованного **набора записей** или объектов **наборов записей** в любой промежуточных предложение COMPUTE или выполнение статистического операций в любого потомка **записей** из ** Набор записей** изменение формы. **Записей** преобразованию и его команды должны использовать же ** объект[подключения](connection-object-ado.md) .


