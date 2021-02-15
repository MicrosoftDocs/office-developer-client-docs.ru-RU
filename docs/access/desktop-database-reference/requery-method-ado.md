---
title: Метод Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306715"
---
# <a name="requery-method-ado"></a>Метод Requery (ADO)

**Область применения**: Access 2013, Office 2013

Обновляет данные в объекте [Recordset](recordset-object-ado.md) с помощью повторного выполнения запроса, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*recordset*. Параметры *requery*

## <a name="parameters"></a>Параметры

|Имя |Описание|
|:----|:----------|
|*Options* |Необязательный параметр. Битоваяmask, которая [содержит значения ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum,](commandtypeenum.md) влияющие на эту операцию.|

> [!NOTE]
> Если *параметру Options* задан **параметр adAsyncExecute,** эта операция будет выполняться асинхронно, и после ее завершения будет выдано событие [RecordsetChangeComplete.](willchangerecordset-and-recordsetchangecomplete-events-ado.md)

Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не следует использовать с **Requery.**

## <a name="remarks"></a>Заметки

Используйте метод **Requery** для обновления всего содержимого объекта **Recordset** из источника данных путем повторной выдачи исходной команды и повторного получения данных. Вызов этого метода эквивалентен вызову методов [Close](close-method-ado.md) и [Open](open-method-ado-recordset.md) последовательно. При редактировании текущей записи или добавлении новой записи возникает ошибка.

Хотя объект **Recordset** открыт, свойства, которые определяют природу курсора ([CursorType,](cursortype-property-ado.md) [LockType,](locktype-property-ado.md) [MaxRecords](maxrecords-property-ado.md)и так далее), являются только для чтения. Таким образом, метод **Requery** может обновить только текущий курсор. Чтобы изменить любое из свойств курсора и просмотреть результаты, необходимо использовать метод [Close,](close-method-ado.md) чтобы свойства снова стали читать и записываться. Затем можно изменить параметры свойства и вызвать метод [Open,](open-method-ado-recordset.md) чтобы повторно открыть курсор.

