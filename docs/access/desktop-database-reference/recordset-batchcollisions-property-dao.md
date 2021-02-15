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

*выражение .* BatchCollisions

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Это свойство содержит массив закладок для строк, которые столкнулись с конфликтом во время последней попытки пакетного вызова **[Update.](recordset-update-method-dao.md)** Свойство **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.

Если для свойства **[bookmark](recordset-bookmark-property-dao.md)** объекта **[Recordset](recordset-object-dao.md)** задаются значения закладок в массиве **BatchCollisions,** можно перейти к каждой записи, которая не прошла последние операции обновления в пакетном режиме.

После исправления записей столкновений можно снова вызвать метод обновления в **пакетном** режиме. На этом этапе DAO пытается повторить пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые не удалось вторую попытку. Все записи, которые были успешными в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified. Этот процесс может продолжаться до тех пор, пока возникают конфликты, или до тех пор, пока вы не закроете набор результатов и откажутся от обновлений.

Этот массив создается повторно при каждом выполнении метода обновления в пакетном **режиме.**

