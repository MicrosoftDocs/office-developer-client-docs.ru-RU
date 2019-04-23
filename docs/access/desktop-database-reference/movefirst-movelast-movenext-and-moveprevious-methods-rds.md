---
title: Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288688"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)

**Область применения**: Access 2013, Office 2013

Перемещение к первой, последней, следующей или предыдущей записи в указанном объекте [Recordset](recordset-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Элемент управления*. Recordset. { MoveFirst | MoveLast | MoveNext | MovePrevious

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|

## <a name="remarks"></a>Замечания

Методы **Move** можно использовать вместе с **RDS. Объект управления** данными для перемещения по записям данных в элементах управления с привязкой к данным на веб-странице. 

Например, предположим, что в сетке отображается **набор записей** с помощью привязки к **RDS. Объект управления** DataObject. Затем можно добавить кнопки "первая", "Последняя", "назад" и "назад", чтобы перейти к первой, последней, следующей или предыдущей записи в отображаемом **наборе записей**. Для этого необходимо вызвать методы **MoveFirst**, **MoveLast**, **MoveNext**и **MovePrevious** объекта **RDS. Объект управления** данные в процедурах OnClick для первой, последней, следующей и предыдущей кнопок соответственно. В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.

