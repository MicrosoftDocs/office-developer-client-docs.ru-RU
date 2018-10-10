---
title: Изменения формы (доступа к рабочему столу ссылку на базу данных)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9e0f8e017e91152ed876b933e0c0c01a7f355e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483259"
---
# <a name="reshaping"></a>Reshaping


**Применимо к**: Access 2013 | Office 2013

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
> <P>Не удается добавить столбцы в существующих <STRONG>записей</STRONG>, изменить форму параметризованного <STRONG>набора записей</STRONG> или объектов <STRONG>наборов записей</STRONG> в любой промежуточных предложение COMPUTE или выполнение статистического операций в любого потомка <STRONG>записей</STRONG> из <STRONG> Набор записей</STRONG> изменение формы. <STRONG>Набор записей</STRONG> преобразованию и новая команда фигуры необходимо использовать то же <A href="connection-object-ado.md">подключение</A>.</P>

