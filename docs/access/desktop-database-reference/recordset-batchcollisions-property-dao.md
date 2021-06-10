---
title: Свойство Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300863"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Свойство Recordset.BatchCollisions (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражения* . BatchCollisions

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Это свойство содержит массив закладок для строк, которые столкнулись с столкновением во время последней попытки пакетного вызова **[обновления.](recordset-update-method-dao.md)** Свойство **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.

Если свойство закладки рабочего объекта **[](recordset-bookmark-property-dao.md)** **[Recordset](recordset-object-dao.md)** задатки закладки в массиве **BatchCollisions,** можно перейти к каждой записи, не завершив последней операции обновления пакетного режима.

После исправления записей столкновений можно снова вызвать метод обновления **пакетного** режима. На этом этапе DAO пытается еще одно пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые потерпели неудачу во второй попытке. Все записи, которые удалось добиться в предыдущей попытке, не отправляются в текущей попытке, так как теперь они имеют свойство **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified. Этот процесс может продолжаться до тех пор, пока возникают столкновения, или до тех пор, пока вы не откажете от обновлений и не закроет набор результатов.

Этот массив повторно создается при каждом выполнении метода обновления **пакетного** режима.

