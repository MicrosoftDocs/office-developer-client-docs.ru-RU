---
title: Свойство NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288555"
---
# <a name="numericscale-property-ado"></a>Свойство NumericScale (ADO)


**Область применения**: Access 2013, Office 2013

Указывает масштаб числовые значения в объекте [Parameter](parameter-object-ado.md) или [Field.](field-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **byte,** которое указывает количество десятичных значений, в которых будут разрешаться числимые значения.

## <a name="remarks"></a>Заметки

Используйте свойство **NumericScale,** чтобы определить, сколько цифр справа от десятичной точки будет использоваться  для представления значений для числимого параметра или объекта **Field.**

Для **объектов Parameter** свойство **NumericScale** имеет свойство read/write.

Для объекта **Field** **NumericScale** обычно имеет только чтение. Однако для новых объектов **Field,** которые были добавлены в коллекцию [Fields](fields-collection-ado.md) записи,  **NumericScale** считывать и записывать только после того,  как свойство [Value](value-property-ado.md) для поля было задано и поставщик данных успешно добавил новое поле путем вызова метода [Update](update-method-ado.md) коллекции **Fields.** [](record-object-ado.md)

