---
title: Объект Field — объекты данных ActiveX (ADO)
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

## <a name="remarks"></a>Замечания

Каждый объект **field** соответствует столбцу в наборе [записей](recordset-object-ado.md). Свойство [value](value-property-ado.md) объекта **field** используется для задания или возвращения данных для текущей записи. В зависимости от функциональных возможностей, предоставляемых поставщиком, некоторые коллекции, методы или свойства объекта **field** могут быть недоступны.

В коллекциях, методах и свойствах объекта **field** можно выполнить следующие действия:

  - Возвращает имя поля со свойством [Name](name-property-ado.md) .

  - Просмотрите или измените данные в поле со свойством **value** . **Value** является свойством по умолчанию объекта **field** .

  - Возвращает основные характеристики поля с помощью свойств [Type](type-property-ado.md), [Precision](precision-property-ado.md)и [NumericScale](numericscale-property-ado.md) .

  - Возврат объявленного размера поля с помощью свойства [DefinedSize](definedsize-property-ado.md) .

  - Возвращает фактический размер данных в заданном поле с помощью свойства [ActualSize](actualsize-property-ado.md) .

  - Определите, какие типы функциональных возможностей поддерживаются для данного поля с помощью [](attributes-property-ado.md) свойства Attributes и коллекции [свойств](properties-collection-ado.md) .

  - Управлять значениями полей с длинными двоичными или длинными символьными данными с помощью [](getchunk-method-ado.md) методов [AppendChunk и](appendchunk-method-ado.md) .

  - Если поставщик поддерживает пакетные обновления, разрешите несоответствия в значениях полей во время пакетного обновления с помощью свойств [originalValue](originalvalue-property-ado.md) и [UnderlyingValue](underlyingvalue-property-ado.md) .

Все свойства метаданных (**Name**, **Type**, **DefinedSize**, **Precision**и **NumericScale**) доступны до открытия **набора записей**объекта **поля** . Их настройка в это время полезна для динамического создания форм.

