---
title: Recordset2.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307492"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражения* . BatchCollisions

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Примечания

Это свойство содержит массив закладок для строк, которые столкнулись с столкновением во время последней попытки пакетного вызова **[обновления.](recordset2-update-method-dao.md)** Свойство **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.

Если свойство закладки рабочего объекта **[](recordset2-bookmark-property-dao.md)** **Recordset** задатки закладки в массиве **BatchCollisions,** можно перейти к каждой записи, не завершив последней операции обновления пакетного режима.

После исправления записей столкновений можно снова вызвать метод обновления **пакетного** режима. На этом этапе DAO пытается еще одно пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые потерпели неудачу во второй попытке. Все записи, которые удалось добиться в предыдущей попытке, не отправляются в текущей попытке, так как теперь они имеют свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** dbRecordUnmodified. Этот процесс может продолжаться до тех пор, пока возникают столкновения, или до тех пор, пока вы не откажете от обновлений и не закроет набор результатов.

Этот массив повторно создается при каждом выполнении метода обновления **пакетного** режима.

