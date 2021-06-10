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

Обновляет данные в текущем объекте [Recordset](recordset-object-ado.md) или [полей](fields-collection-ado.md) объекта [Record](record-object-ado.md) из баз данных.

## <a name="syntax"></a>Синтаксис

*Recordset*. Resync *AffectRecords*, *ResyncValues*

*Запись*. *Поля*. Resync *ResyncValues*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*AffectRecords* |Необязательный параметр. Значение [AffectEnum,](affectenum.md) которое определяет количество записей, на которые повлияет метод **Resync.** По умолчанию значение **adAffectAll**. Это значение не доступно с методом **Resync** коллекции **Полей** объекта **Record.**|
|*ResyncValues* |Необязательный параметр. Значение [ResyncEnum,](resyncenum.md) которое указывает, перезаписаны ли эти значения. По умолчанию значение **adResyncAllValues**.|

## <a name="remarks"></a>Примечания

### <a name="recordset"></a>Recordset

Используйте метод **Resync** для повторной синхронизации записей в текущем **наборе записей** с базой данных. Это полезно, если вы используете курсор статического или только для вперед, но вы хотите увидеть какие-либо изменения в баз данных.

Если задайте свойство [CursorLocation](cursorlocation-property-ado.md) **adUseClient,** **Resync** доступен только для объектов **Recordset,** не доступных только для чтения.

В отличие [от метода Requery,](requery-method-ado.md) метод **Resync** не выполняет команду, основанную на объекте **Recordset.** Новые записи в баз данных не будут видны.

Если попытка ресинхронизации не удалась из-за конфликта с данными( например, запись была удалена другим пользователем), [](errors-collection-ado.md) поставщик возвращает предупреждения в коллекцию Ошибок и возникает ошибка во время работы. Используйте свойство [Filter](filter-property-ado.md) **(adFilterConflictingRecords)** и свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.

Если динамические свойства Unique [Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и [Resync Command](resync-command-property-dynamic-ado.md) заданы, а набор **recordset** является результатом выполнения операции JOIN на нескольких таблицах, то метод **Resync** будет выполнять команду, заданную в свойстве Команды **Resync** только на таблице, названной в свойстве **Unique Table.**

### <a name="fields"></a>Fields

Используйте метод **Resync,** чтобы ресинхронизировать значения коллекции **Полей** объекта **Record** с исходным источником данных. Свойство [Count](count-property-ado.md) не влияет на этот метод.

Если *значение ResyncValues* установлено для **adResyncAllValues** (значение по умолчанию), то свойства [UnderlyingValue,](underlyingvalue-property-ado.md) [Value](value-property-ado.md)и [OriginalValue](originalvalue-property-ado.md) объектов [Field](field-object-ado.md) в коллекции синхронизируются. Если *для ResyncValues* **установлено свойство adResyncUnderlyingValues,** синхронизируется только свойство **UnderlyingValue.**

Значение свойства **Status** для каждого объекта **Field** во время вызова также влияет на поведение **Resync.** Для **объектов Field** **со** значениями состояния **adFieldPendingUnknown** или **adFieldPendingInsert** **resync** не влияет. Для **значений** состояния **adFieldPendingChange** или **adFieldPendingDelete** **Resync** синхронизирует значения данных для полей, которые по-прежнему существуют в источнике данных.

**Resync** не будет изменять значения **состояния** объектов **Field,** если при вызвании **Resync** не произойдет ошибка. Например, если поле больше не существует, поставщик  возвращает соответствующее значение Status для объекта **Field,** например **adFieldDoesNotExist.** **Возвращаемые** значения состояния могут логически сочетаться в значении свойства **Status.**

