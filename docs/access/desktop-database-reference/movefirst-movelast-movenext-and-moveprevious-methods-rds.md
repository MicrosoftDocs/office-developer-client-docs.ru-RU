---
title: Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c78e6aaca31201e076dffb55b19be638a337dd19
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944930"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)


**Применимо к**: Access 2013, Office 2013

Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте [набора записей](recordset-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*DataControl*. Набор записей. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

## <a name="remarks"></a>Примечания

Можно использовать методы **перемещения** с **RDS. DataControl** объекта для перехода по записям данных в элементах управления с привязкой к данным на веб-страницы. Например предположим, что отображение **записей** в таблице путем привязки к **RDS. DataControl** объекта. Первый, последний, Далее и назад кнопки, которая используется для перемещения на первый, последний, далее, затем можно включить или предыдущей записи в отображаемой **набора записей**. Это делается путем вызова **MoveFirst**, **MoveLast**, **MoveNext**и методы **MovePrevious** **RDS. DataControl** объект в процедуры onClick для кнопки первый, последний, Далее и назад, соответственно. В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.

