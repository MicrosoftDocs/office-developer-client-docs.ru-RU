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

Добавляет данные в [поле](field-object-ado.md)большого текста или двоичных данных или в объект [Parameter](parameter-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*объект.* *Данные* AppendChunk

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*object* |Объект **field** или **Parameter** .|
|*Data* |**Переменная типа Variant** , содержащая данные, которые необходимо добавить в объект.|

## <a name="remarks"></a>Примечания

Используйте метод **AppendChunk** для **поля** или объекта **Parameter** , чтобы заполнить его длинными двоичными или символьными данными. В ситуациях, когда ограничена системная память, можно использовать метод **AppendChunk** для управления длинными значениями в частях, а не целиком.

### <a name="field"></a>Поле

Если для бита **адфлдлонг** в свойстве [Attribute](attributes-property-ado.md) объекта **field** задано значение true, можно использовать метод **AppendChunk** для этого поля.

Первый вызов **AppendChunk** для объекта **field** записывает данные в поле, перезаписывая существующие данные. Последующие вызовы **AppendChunk** добавляются к существующим данным. Если вы добавляете данные в одно поле, а затем задаете или просматриваете значение другого поля в текущей записи, ADO считает, что вы завершили добавление данных в первое поле. Если вызвать метод **AppendChunk** для первого поля еще раз, ADO интерпретирует вызов как новую операцию **AppendChunk** и перезаписывает существующие данные. Доступ к полям в других объектах [Recordset](recordset-object-ado.md) , которые не являются клонами первого объекта **Recordset** , не приводит к нарушению операций **AppendChunk** .

Если при вызове **AppendChunk** для объекта **field** отсутствует текущая запись, возникает ошибка.

> [!NOTE]
> Метод **AppendChunk** не работает с объектами **field** объекта [Record](record-object-ado.md) . Она не выполняет никаких операций и создает ошибку во время выполнения.

### <a name="parameters"></a>Параметры

Если бит **адпарамлонг** в свойстве **Attributes** объекта **Parameter** имеет значение true, можно использовать метод **AppendChunk** для этого параметра.

Первый вызов **AppendChunk** для объекта **Parameter** записывает данные в параметр, перезаписывая существующие данные. Последующие вызовы **AppendChunk** для объекта **Parameter** добавляют существующие данные параметров. Вызов **AppendChunk** , который передает значение null, отклоняет все данные параметра.

