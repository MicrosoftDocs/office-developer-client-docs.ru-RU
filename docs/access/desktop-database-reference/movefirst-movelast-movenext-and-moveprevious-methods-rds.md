---
title: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481655"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)


**Применимо к**: Access 2013 | Office 2013

Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте [набора записей](recordset-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*DataControl*. Набор записей. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

## <a name="remarks"></a>Замечания

Можно использовать методы **перемещения** с **RDS. DataControl** объекта для перехода по записям данных в элементах управления с привязкой к данным на веб-странице. Например предположим, что отображение **записей** в таблице путем привязки к **RDS. DataControl** объекта. Первый, последний, Далее и назад кнопки, которая используется для перемещения на первый, последний, далее, затем можно включить или предыдущей записи в отображаемой **набора записей**. Это делается путем вызова **MoveFirst**, **MoveLast**, **MoveNext**и методы **MovePrevious** **RDS. DataControl** объект в процедуры onClick для кнопки первый, последний, Далее и назад, соответственно. В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.

