---
title: Метод Resync (ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fa483d86dc345968607a0752f0552ddccfe7fef5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306575"
---
# <a name="resync-method-ado"></a>Метод Resync (ADO)

**Область применения**: Access 2013, Office 2013

Обновляет данные в текущем объекте [Recordset](recordset-object-ado.md) или коллекции [Fields](fields-collection-ado.md) объекта [Record](record-object-ado.md) из базы данных.

## <a name="syntax"></a>Синтаксис

*Recordset*. Resync *AffectRecords*, *ResyncValues*

*Запись*. *Поля*. Resync *ResyncValues*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*AffectRecords* |Необязательный параметр. Значение [AffectEnum,](affectenum.md) которое определяет, сколько записей влияет на метод **Resync.** Значение по умолчанию **— adAffectAll.** Это значение не доступно в **методе Resync** коллекции **Fields** объекта **Record.**|
|*ResyncValues* |Необязательный параметр. Значение [ResyncEnum,](resyncenum.md) которое указывает, перезаписываются ли значения. Значение по умолчанию **— adResyncAllValues.**|

## <a name="remarks"></a>Заметки

### <a name="recordset"></a>Recordset

Используйте метод **Resync** для повторной синхронизации записей в текущем наборе **записей** с базой данных. Это полезно, если вы используете статический курсор или курсор "только вперед", но хотите увидеть любые изменения в базе данных.

Если для свойства [CursorLocation](cursorlocation-property-ado.md) установлено свойство **adUseClient,** **Resync** доступен только для объектов **Recordset,** не доступных только для чтения.

В отличие [от метода Requery,](requery-method-ado.md) метод **Resync** не выполняет команду, которая находится в основном объекте **Recordset.** Новые записи в базе данных не будут видны.

Если попытка повторной синхронизации не удалась из-за конфликта с данными, которые были удалены другим пользователем (например, запись [](errors-collection-ado.md) была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию ошибок и возникает ошибка во время работы. Используйте свойство [Filter](filter-property-ado.md) **(adFilterConflictingRecords)** и свойство [Status](status-property-ado-recordset.md) для поиска записей с конфликтами.

Если заданы динамические свойства Unique [Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и [Resync Command,](resync-command-property-dynamic-ado.md) а **recordset** является результатом выполнения операции JOIN в нескольких таблицах, то метод **Resync** будет выполнять команду, предоставленную в свойстве **Resync Command,** только в таблице, именуемой в свойстве **Unique Table.**

### <a name="fields"></a>Поля

Используйте метод **Resync** для повторной синхронизации значений коллекции **Fields** объекта **Record** с помощью источника данных. На [свойство Count](count-property-ado.md) этот метод не влияет.

Если *для ResyncValues* установлено значение **adResyncAllValues** (значение по умолчанию), синхронизируются свойства [UnderlyingValue,](underlyingvalue-property-ado.md) [Value](value-property-ado.md)и [OriginalValue](originalvalue-property-ado.md) объектов [Field](field-object-ado.md) в коллекции. Если *для ResyncValues* установлено свойство **adResyncUnderlyingValues,** синхронизируется только свойство **UnderlyingValue.**

Значение свойства **Status** для каждого **объекта Field** во время вызова также влияет на поведение **Resync.** Для **объектов Field** **со** значениями состояния **adFieldPendingUnknown** или **adFieldPendingInsert** **resync** не действует. Для **значений** состояния **adFieldPendingChange** или **adFieldPendingDelete** **Resync** синхронизирует значения данных для полей, которые все еще существуют в источнике данных.

**Resync** не будет изменять значения **состояния** объектов **Field,** если только не произойдет ошибка при ее под названием **Resync.** Например, если поле больше не существует, поставщик возвращает соответствующее значение **состояния** для объекта **Field,** например **adFieldDoesNotExist.** **Возвращаемая величина** состояния может логически сочетаться в значении **свойства Status.**

