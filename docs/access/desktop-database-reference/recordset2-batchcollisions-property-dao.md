---
title: Recordset2.BatchCollisions property (DAO)
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
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions property (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* BatchCollisions

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Заметки

Это свойство содержит массив закладок для строк, которые столкнулись с конфликтом во время последней попытки пакетного вызова **[Update.](recordset2-update-method-dao.md)** Свойство **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.

Если для свойства **[bookmark](recordset2-bookmark-property-dao.md)** объекта **Recordset** задаются значения закладок в массиве **BatchCollisions,** можно перейти к каждой записи, которая не прошла последние операции обновления в пакетном режиме.

После исправления записей столкновений можно снова вызвать метод обновления в **пакетном** режиме. На этом этапе DAO пытается повторить пакетное обновление, и свойство **BatchCollisions** снова отражает набор записей, которые не удалось вторую попытку. Все записи, которые были успешными в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[RecordStatus](recordset2-recordstatus-property-dao.md)** dbRecordUnmodified. Этот процесс может продолжаться до тех пор, пока возникают конфликты, или до тех пор, пока вы не закроете набор результатов и откажутся от обновлений.

Этот массив создается повторно при каждом выполнении метода обновления в пакетном **режиме.**

