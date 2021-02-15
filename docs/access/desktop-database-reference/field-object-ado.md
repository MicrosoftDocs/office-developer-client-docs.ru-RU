---
title: Field Object - ActiveX Data Objects (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2bf17029a706ad6902a8a01a14e73183f94d7a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293058"
---
# <a name="field-object-ado"></a>Объект Field (ADO)


**Область применения**: Access 2013, Office 2013

Представляет столбец данных с общим типом данных.

## <a name="remarks"></a>Заметки

Каждый объект **Field** соответствует столбцу в [наборе записей.](recordset-object-ado.md) Свойство [Value](value-property-ado.md) объектов **Field** используется для того, чтобы устанавливать или возвращать данные для текущей записи. В зависимости от функциональных возможностей, доступных поставщиком, некоторые коллекции, методы или свойства объекта **Field** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Field** можно сделать следующее:

  - Возвращает имя поля со [свойством Name.](name-property-ado.md)

  - Просмотр или изменение данных в поле с помощью свойства **Value.** **Значение** является свойством по умолчанию объекта **Field.**

  - Возвращает основные характеристики поля со свойствами [Type,](type-property-ado.md) [Precision](precision-property-ado.md)и [NumericScale.](numericscale-property-ado.md)

  - Возвращает объявленный размер поля со [свойством DefinedSize.](definedsize-property-ado.md)

  - Возвращает фактический размер данных в заданное поле со [свойством ActualSize.](actualsize-property-ado.md)

  - Определите, какие типы функций поддерживаются для заданного поля с помощью свойства [Attributes](attributes-property-ado.md) и [коллекции свойств.](properties-collection-ado.md)

  - Управляет значениями полей, содержащих длинные двоичные или длинные данные символов, с помощью методов [AppendChunk](appendchunk-method-ado.md) и [GetChunk.](getchunk-method-ado.md)

  - Если поставщик поддерживает пакетные обновления, разрешать несоответствия в значениях полей во время пакетного обновления со свойствами [OriginalValue](originalvalue-property-ado.md) и [UnderlyingValue.](underlyingvalue-property-ado.md)

Все свойства метаданных (**Name,** **Type,** **DefinedSize,** **Precision** и **NumericScale)**  доступны перед открытием объекта **Recordset объекта Field.** Установка их в это время полезна для динамического создания форм.

