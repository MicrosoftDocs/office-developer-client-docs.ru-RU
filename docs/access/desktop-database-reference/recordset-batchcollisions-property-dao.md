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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700375"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Свойство Recordset.BatchCollisions (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . BatchCollisions

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

Это свойство содержит массив закладки строк, которые столкнулись с конфликтом во время последнего вызова **[обновления](recordset-update-method-dao.md)** попытка пакета. Свойство **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** указывает число элементов в массиве.

Если значение рабочего объекта **[набора записей](recordset-object-dao.md)** свойства **[Bookmark](recordset-bookmark-property-dao.md)** значений закладку в массиве **BatchCollisions** , можно переместить в каждой записи, которая не удалось завершить последнюю операцию обновления пакетного режима.

После исправления записей конфликта пакетном режиме метод **Update** можно позвонить еще раз. На этом этапе DAO пытается другого пакета обновления, и свойство **BatchCollisions** еще раз отражает набора записей, которые не удалось второй раз. Записи, в которых завершена успешно Предыдущая попытка не отправляются в текущем попытки как теперь у них есть свойство **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified. Этот процесс может продолжаться до тех пор, пока происходит конфликт или пока отказаться от обновления и закройте набора результатов.

Этот массив повторно создается при каждом выполнении метода **Update** пакетном режиме.

