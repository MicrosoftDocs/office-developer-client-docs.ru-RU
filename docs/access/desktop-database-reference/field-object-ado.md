---
title: Объект field — ActiveX объектов данных (ADO)
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

## <a name="remarks"></a>Примечания

Каждый объект **Field** соответствует столбцу в [Наборе записей.](recordset-object-ado.md) Свойство [Value](value-property-ado.md) объектов **Field** используется для набора или возврата данных для текущей записи. В зависимости от функциональных возможностей, которые предоставляет поставщик, некоторые коллекции, методы или свойства объекта **Field** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Field** можно сделать следующее:

  - Возвращаем имя поля с [свойством Name.](name-property-ado.md)

  - Просмотр или изменение данных в поле с помощью **свойства Value.** **Значение** — это свойство по умолчанию объекта **Field.**

  - Верни основные характеристики поля с свойствами [Type,](type-property-ado.md) [Precision](precision-property-ado.md)и [NumericScale.](numericscale-property-ado.md)

  - Возврат объявленного размера поля с [свойством DefinedSize.](definedsize-property-ado.md)

  - Возврат фактического размера данных в заданное поле с помощью [свойства ActualSize.](actualsize-property-ado.md)

  - Определите, какие типы функций поддерживаются для данного поля с помощью коллекции свойств и [свойств](properties-collection-ado.md) [Attributes.](attributes-property-ado.md)

  - Манипулировать значениями полей, содержащих длинные двоичные или длинные данные символов с помощью методов [AppendChunk](appendchunk-method-ado.md) и [GetChunk.](getchunk-method-ado.md)

  - Если поставщик поддерживает пакетные обновления, устранять несоответствия в значениях полей при пакетном обновлении с свойствами [OriginalValue](originalvalue-property-ado.md) и [UnderlyingValue.](underlyingvalue-property-ado.md)

Все свойства метаданных **(Name,** **Type,** **DefinedSize,** **Precision** и **NumericScale)** доступны  перед открытием наборов **записей объекта Field.** Установка их в это время полезна для динамического построения форм.

