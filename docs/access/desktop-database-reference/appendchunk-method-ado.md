---
title: Метод AppendChunk (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89a75ebe8a3fe704c4f755a0f744eac4d068ec0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297027"
---
# <a name="appendchunk-method-ado"></a>Метод AppendChunk (ADO)

**Область применения**: Access 2013, Office 2013

Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.

## <a name="syntax"></a>Синтаксис

*object.* Данные AppendChunk 

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*object* |Объект **Field** или **Parameter.**|
|*Data* |**Вариант,** содержащий данные, которые необходимо примедить к объекту.|

## <a name="remarks"></a>Заметки

Используйте метод **AppendChunk** для объекта **Field** или **Parameter,** чтобы заполнить его длинными двоичными или символьными данными. В ситуациях, когда системная память ограничена, можно использовать метод **AppendChunk** для управления длинными значениями по частям, а не полностью.

### <a name="field"></a>Поле

Если бит **adFldLong** в свойстве [Attributes](attributes-property-ado.md) объекта **Field** имеет true, можно использовать метод **AppendChunk** для этого поля.

Первый вызов **AppendChunk** для объекта **Field** записывает данные в поле, переописав все существующие данные. Последующие **вызовы AppendChunk** добавляются в существующие данные. Если вы при добавлении данных в одно поле и затем установили или считыали значение другого поля в текущей записи, ADO предполагает, что вы завершили добавление данных в первое поле. При повторном вызове метода **AppendChunk** в первом поле ADO интерпретирует вызов как новую операцию **AppendChunk** и переоценит существующие данные. Доступ к полям в других [объектах Recordset,](recordset-object-ado.md) которые не являются клонами первого объекта **Recordset,** не нарушит операции **AppendChunk.**

Если при вызове **AppendChunk** для объекта **Field** нет текущей записи, возникает ошибка.

> [!NOTE]
> Метод **AppendChunk** не работает с **объектами Field** объекта [Record.](record-object-ado.md) Он не выполняет никаких операций и создает ошибку во время выполнения.

### <a name="parameters"></a>Параметры

Если бит **adParamLong** в свойстве **Attributes** объекта **Parameter** имеет true, для этого параметра можно использовать метод **AppendChunk.**

Первый вызов **AppendChunk** для объекта **Parameter** записывает данные в параметр, переописав все существующие данные. Последующие **вызовы AppendChunk** для объекта **Parameter** добавляются к существующим данным параметра. Вызов **AppendChunk,** который передает значение null, удаляет все данные параметра.

