---
title: Свойство IsolationLevel (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291151"
---
# <a name="isolationlevel-property-ado"></a>Свойство IsolationLevel (ADO)


**Область применения**: Access 2013, Office 2013

Указывает уровень изоляции для объекта [Подключения.](connection-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение [IsolationLevelEnum.](isolationlevelenum.md) По умолчанию **это adXactChaos.**

## <a name="remarks"></a>Примечания

Используйте свойство **IsolationLevel,** чтобы установить уровень изоляции объекта **Подключения.** Параметр не вступает в силу до следующего вызова метода [BeginTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md) Если запрашиваемый уровень изоляции недоступен, поставщик может вернуть следующий более высокий уровень изоляции.

Свойство **IsolationLevel** — это чтение и написание.

**Удаленное использование службы данных** При этом свойство **IsolationLevel** может быть задавано только **adXactUnspecified.**

Поскольку пользователи работают с отключенными объектами **Recordset** в клиентском кэше, могут возникнуть проблемы с несколькими пользователями. Например, когда два разных пользователя пытаются обновить ту же запись, служба удаленных данных просто позволяет пользователю, который сначала обновляет запись, "выиграть". Второй запрос обновления пользователя не будет работать с ошибкой.

