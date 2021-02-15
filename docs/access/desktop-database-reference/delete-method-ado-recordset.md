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

*recordset*. Удаление *AffectRecords*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*AffectRecords* |Значение [AffectEnum,](affectenum.md) которое определяет количество записей, на которые влияет метод **Delete.** Значение по умолчанию **— adAffectCurrent.**|

> [!NOTE]
> **adAffectAll** и **adAffectAllChapters** не являются допустимыми аргументами для **удаления.**

## <a name="remarks"></a>Заметки

Метод **Delete** пометит текущую запись или группу записей в [объекте Recordset](recordset-object-ado.md) для удаления. Если объект **Recordset** не разрешает удаление записей, возникает ошибка. Если вы находитесь в режиме немедленного обновления, немедленное удаление происходит в базе данных. Если запись не удается успешно удалить (например, из-за нарушений целостности базы данных), запись останется в режиме редактирования после вызова **"Обновить".** Это означает, что перед перемещением текущей записи (например, с [close,](close-method-ado.md) [Move](move-method-ado.md)или [NextRecordset)](nextrecordset-method-ado.md)необходимо отменить обновление с помощью [CancelUpdate.](cancelupdate-method-ado.md)

Если вы находитесь в режиме пакетного обновления, записи помечаются для удаления из кэша, а фактическое удаление происходит при вызове метода [UpdateBatch.](updatebatch-method-ado.md) (Используйте свойство [Filter](filter-property-ado.md) для просмотра удаленных записей.)

При искомом значении поля из удаленной записи создается ошибка. После удаления текущей записи удаленная запись остается текущей, пока вы не перейдете к другой записи. После перемещения от удаленной записи она будет недоступна.

При вложении удалений в транзакцию можно восстановить удаленные записи с помощью метода [RollbackTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md) Если вы находитесь в режиме пакетного обновления, вы можете отменить ожидающих удаления или группу ожидающих удаления с помощью метода [CancelBatch.](cancelbatch-method-ado.md)

Если попытка удалить записи не удалась из-за конфликта с данными, которые находятся в ее реализации (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию [ошибок,](errors-collection-ado.md) но не останавливает выполнение программы. Ошибка во время запуска возникает только при конфликтах всех запрашиваемых записей.

Если за установлено динамическое свойство Unique [Table,](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) а **recordset** является результатом выполнения операции JOIN в нескольких таблицах, метод **Delete** удаляет только строки из таблицы, именуемой в свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)

