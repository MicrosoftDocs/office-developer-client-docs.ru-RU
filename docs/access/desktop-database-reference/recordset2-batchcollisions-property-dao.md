---
title: Recordset2.BatchCollisions Property (DAO)
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
ms.openlocfilehash: 204b66b120405522707da23bf093a311ca8c2625
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481569"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions Property (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . BatchCollisions

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Это свойство содержит массив закладки строк, которые столкнулись с конфликтом во время последнего вызова **[обновления](recordset2-update-method-dao.md)** попытка пакета. Свойство **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** указывает число элементов в массиве.

Если значение рабочего объекта **набора записей** свойства **[Bookmark](recordset2-bookmark-property-dao.md)** значений закладку в массиве **BatchCollisions** , можно переместить в каждой записи, которая не удалось завершить последнюю операцию обновления пакетного режима.

После исправления записей конфликта пакетном режиме метод **Update** можно позвонить еще раз. На этом этапе DAO пытается другого пакета обновления, и свойство **BatchCollisions** еще раз отражает набора записей, которые не удалось второй раз. Записи, в которых завершена успешно Предыдущая попытка не отправляются в текущем попытки как теперь у них есть свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** dbRecordUnmodified. Этот процесс может продолжаться до тех пор, пока происходит конфликт или пока отказаться от обновления и закройте набора результатов.

Этот массив повторно создается при каждом выполнении метода **Update** пакетном режиме.

