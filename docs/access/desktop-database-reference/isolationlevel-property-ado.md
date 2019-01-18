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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698871"
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

