---
title: Метод CancelBatch (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 832b367824fd8043486ff85f63739c3288696774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296642"
---
# <a name="cancelbatch-method-ado"></a>Метод CancelBatch (ADO)

**Область применения**: Access 2013, Office 2013

Отмена ожидающих пакетных обновлений.

## <a name="syntax"></a>Синтаксис

*набор записей.* CancelBatch *AffectRecords*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*AffectRecords* |Необязательный параметр. Значение [AffectEnum,](affectenum.md) которое указывает, сколько записей повлияет на метод **CancelBatch.** |

## <a name="remarks"></a>Примечания

Используйте метод **CancelBatch** для отмены ожидающих обновлений в [наборе записей](recordset-object-ado.md) в режиме пакетного обновления. Если Набор **записей находится** в режиме немедленного обновления, вызов **CancelBatch** без **adAffectCurrent** создает ошибку.

Если вы редактируете текущую запись или добавляете новую запись при вызове **CancelBatch,** ADO сначала вызывает метод [CancelUpdate,](cancelupdate-method-ado.md) чтобы отменить любые кэшированые изменения. После этого все ожидающих изменений **в Наборе записей** отменяются.

Возможно, текущая запись будет неопределима после вызова **CancelBatch,** особенно если вы были в процессе добавления новой записи. По этой причине целесообразно установить текущее положение записи в известном расположении в **Наборе** записей после вызова **CancelBatch.** Например, позвоните [методу MoveFirst.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)

Если попытка отменить ожидающие обновления не удалась из-за конфликта с данными( например, запись была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию Ошибок, но не прекращает выполнение программы. [](errors-collection-ado.md) Ошибка во время запуска возникает только в том случае, если во всех запрашиваемых записях имеются конфликты. Используйте свойство [Filter](filter-property-ado.md) **(adFilterAffectedRecords)** и свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.

