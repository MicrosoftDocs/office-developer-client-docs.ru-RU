---
title: Метод Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0105fb67c095355e607c6c73fc73fc4c6b1050ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998196"
---
# <a name="requery-method-ado"></a>Метод Requery (ADO)

**Применимо к**: Access 2013, Office 2013

Обновляет данные в объект [набора записей](recordset-object-ado.md) , повторное выполнение запросов, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*набор записей*. Обновление *параметров*

## <a name="parameters"></a>Параметры

|Имя |Описание|
|:----|:----------|
|*Варианты* |Необязательно указывать. Битовая маска, которая содержит значения [ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum](commandtypeenum.md) влияния на этой операции.|

> [!NOTE]
> Если *Параметры* **adAsyncExecute**, эта операция выполняется асинхронно и события [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) будет выдается, когда она завершается.

Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не должен использоваться с **повторный запрос**.

## <a name="remarks"></a>Примечания

Используйте метод **повторный запрос** для обновления все содержимое объекта **набора записей** из источника данных путем получения исходного команды и извлечение данных еще раз. Вызов данного метода эквивалентен вызову метода [Close](close-method-ado.md) и [открытия](open-method-ado-recordset.md) последовательно. Если вы изменяете текущей записи или добавлять новую запись, возникает ошибка.

Когда открыт объекта **набора записей** , свойства, которые определяют характер курсор ([CursorType](cursortype-property-ado.md), [LockType для](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md)и т. д.) доступны только для чтения. Таким образом метод **повторный запрос** можно только обновить курсора. Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства становятся чтение и запись еще раз. Затем можно изменить значения свойств и вызвать метод [Open](open-method-ado-recordset.md) , чтобы снова открыть курсор.

