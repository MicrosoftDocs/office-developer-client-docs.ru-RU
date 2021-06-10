---
title: Метод Delete (Recordset в ADO)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8142d4fc4fc0036f80693f0bff779d9f3f2a62e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294101"
---
# <a name="delete-method-ado-recordset"></a>Метод Delete (Recordset в ADO)

**Область применения**: Access 2013, Office 2013

Удаляет текущую запись или группу записей.

## <a name="syntax"></a>Синтаксис

*набор записей.* Удаление *AffectRecords*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*AffectRecords* |Значение [AffectEnum,](affectenum.md) определя которое определяет количество записей, на которые повлияет метод **Delete.** По умолчанию значение **adAffectCurrent**.|

> [!NOTE]
> **adAffectAll и** **adAffectAllChapters** не являются допустимым аргументом для **удаления**.

## <a name="remarks"></a>Примечания

Метод **Delete** отмечает текущую запись или группу записей в [объекте Recordset](recordset-object-ado.md) для удаления. Если объект **Recordset** не разрешает удаление записей, возникает ошибка. Если вы находитесь в режиме немедленного обновления, в базе данных немедленно происходят удаления. Если запись не удается успешно удалить (например, из-за нарушений целостности базы данных), запись останется в режиме редактирования после вызова **обновления.** Это означает, что необходимо отменить обновление с [помощью CancelUpdate,](cancelupdate-method-ado.md) прежде чем отменить текущую запись (например, с [Close,](close-method-ado.md) [Move](move-method-ado.md)или [NextRecordset).](nextrecordset-method-ado.md)

Если вы находитесь в режиме пакетного обновления, записи помечены для удаления из кэша, а фактическое удаление происходит при вызове метода [UpdateBatch.](updatebatch-method-ado.md) (Используйте свойство [Filter](filter-property-ado.md) для просмотра удаленных записей.)

Удаление значений поля из удаленной записи создает ошибку. После удаления текущей записи удаленная запись остается текущей до тех пор, пока вы не перейдете к другой записи. После удаления от удаленной записи она больше недоступна.

При вложении удалений в транзакцию можно восстановить удаленные записи с помощью метода [RollbackTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md) Если вы находитесь в режиме пакетного обновления, можно отменить ожидающих удаления или группу ожидающих удалений с помощью метода [CancelBatch.](cancelbatch-method-ado.md)

Если попытка удалить записи не удалась из-за конфликта с данными( например, запись уже удалена другим пользователем), [](errors-collection-ado.md) поставщик возвращает предупреждения в коллекцию Ошибок, но не прекращает выполнение программы. Ошибка во время запуска возникает только в том случае, если во всех запрашиваемых записях имеются конфликты.

Если [динамическое](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) свойство Unique Table установлено, а набор **recordset** является результатом выполнения операции JOIN на нескольких таблицах, метод **Delete** удаляет строки из таблицы, названной в свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)

