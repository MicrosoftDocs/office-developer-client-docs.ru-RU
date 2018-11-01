---
title: Свойство IsolationLevel (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76978d33fc5f82c9b1f8137b64a663e7e95f2204
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883059"
---
# <a name="isolationlevel-property-ado"></a>Свойство IsolationLevel (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает уровень изоляции для объекта [подключения](connection-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [IsolationLevelEnum](isolationlevelenum.md) . Значение по умолчанию — **adXactChaos**.

## <a name="remarks"></a>Замечания

Используйте свойство **IsolationLevel** , чтобы установить уровень изоляции объект **подключения** . Параметр не вступят в силу только при следующем вызове метода [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) . Если уровень изоляции, которые вы запрашиваете недоступен, поставщик может возвращать Далее больший уровень изоляции.

Свойство **IsolationLevel** — чтение и запись.

**Службы удаленных данных об использовании** При использовании на объект подключения со стороны клиента, свойство **IsolationLevel** можно задать только к **adXactUnspecified**.

Так как пользователей работе с отключенных объектов **наборов записей** в кэш со стороны клиента, может быть многопользовательской проблемы. Например попытку обновления одной записи двух различных пользователей удаленной службы данных просто позволяет пользователю, сначала обновляет запись «win». Запрос на обновление второго пользователя завершится с ошибкой.

