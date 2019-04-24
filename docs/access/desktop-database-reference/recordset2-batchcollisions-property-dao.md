---
title: Свойство Recordset2. Батчколлисионс (DAO)
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
# <a name="recordset2batchcollisions-property-dao"></a>Свойство Recordset2. Батчколлисионс (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Батчколлисионс

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

Это свойство содержит массив закладок на строки, которые вызвали конфликт во время последнего попытки вызова пакетного **[обновления](recordset2-update-method-dao.md)** . Свойство **[батчколлисионкаунт](recordset2-batchcollisioncount-property-dao.md)** указывает количество элементов в массиве.

Если присвоить свойству **[закладки](recordset2-bookmark-property-dao.md)** рабочего объекта **Recordset** значения закладки в массиве **батчколлисионс** , можно перейти к каждой записи, которая не смогла выполнить последнюю операцию обновления в пакетном режиме.

После исправления записей о конфликтах можно снова вызвать метод обновления в режиме пакетного **обновления** . На этом шаге DAO предпринимает попытку выполнить еще одно пакетное обновление, а свойство **батчколлисионс** еще раз отражает набор записей, которые не удалось выполнить вторую попытку. Все записи, которые были успешно выполнены в предыдущей попытке, не отправляются в текущей попытке, так как теперь у них есть свойство **[Рекордстатус](recordset2-recordstatus-property-dao.md)** дбрекордунмодифиед. Этот процесс может продолжаться до тех пор, пока не будут выполнены конфликты, или пока не будут отменены все изменения и закрыть результирующий набор.

Этот массив повторно создается каждый раз при выполнении метода **обновления** в пакетном режиме.

