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

Перемещается к первой, последней, следующей или предыдущей записи в указанном [объекте Recordset.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

*DataControl*. Recordset. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|

## <a name="remarks"></a>Заметки

С RDS **можно** использовать методы **Move. Объект DataControl** для навигации по записям данных в привязанных к данным элементов управления на веб-странице. 

Например, предположим, что набор **записей** отображается в сетке путем привязки к **RDS. Объект DataControl.** Затем можно включить кнопки "Первая", "Последняя", "Далее" и "Предыдущая", которые пользователи могут нажать, чтобы перейти к первой, последней, следующей или предыдущей записи в отображаемом наборе **записей.** Для этого необходимо вызывать методы **MoveFirst,** **MoveLast,** **MoveNext** и **MovePrevious** **служб RDS. Объект DataControl** в процедурах onClick для кнопок First, Last, Next и Previous соответственно. В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.

