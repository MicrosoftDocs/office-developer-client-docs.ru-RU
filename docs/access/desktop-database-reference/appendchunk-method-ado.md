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

Придает данные большому текстовом или двоичному [поле](field-object-ado.md)данных или [объекту Parameter.](parameter-object-ado.md)

## <a name="syntax"></a>Синтаксис

*объект.* Данные appendChunk 

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*object* |Объект **Field** или **Parameter.**|
|*Data* |**Вариант,** содержащий данные для приложения к объекту.|

## <a name="remarks"></a>Примечания

Используйте метод **AppendChunk** на **объекте Field** или **Parameter,** чтобы заполнить его длинными двоичными или характерными данными. В ситуациях, когда память системы ограничена, можно использовать метод **AppendChunk** для обработки длинных значений частями, а не целиком.

### <a name="field"></a>Поле

Если бит **adFldLong** в свойстве [Атрибуты](attributes-property-ado.md) объекта **Field** задан для true, для этого поля можно использовать метод **AppendChunk.**

Первый вызов **AppendChunk на** объект **Field** записывает данные в поле, переописав все существующие данные. Последующие **вызовы AppendChunk** добавляются к существующим данным. Если вы примыкаете к одному полю, а затем задайте или считывая значение другого поля в текущей записи, ADO предполагает, что вы закончили приложение данных к первому полю. Если снова вызвать метод **AppendChunk** в первом поле, ADO интерпретирует вызов как новую операцию **AppendChunk** и переопределает существующие данные. Доступ к полям в других [объектах Recordset,](recordset-object-ado.md) которые не являются клонами первого объекта **Recordset,** не будет нарушать операции **AppendChunk.**

Если при вызове **AppendChunk** на объект **Field** нет текущей записи, возникает ошибка.

> [!NOTE]
> Метод **AppendChunk** не работает на **объектах Field** объекта [Record.](record-object-ado.md) Он не выполняет никаких операций и создает ошибку во время выполнения.

### <a name="parameters"></a>Parameters

Если бит **adParamLong** в свойстве **Атрибуты** объекта **Parameter** настроен на верность, для этого параметра можно использовать метод **AppendChunk.**

Первый вызов **AppendChunk на** **объекте Parameter** записывает данные в параметр, переописыв все существующие данные. Последующие **вызовы AppendChunk** на **объекте Parameter** добавляются к существующим данным параметров. Вызов **AppendChunk,** который передает значение null, удаляет все данные параметров.

