---
title: Поле объекта - ActiveX Data Objects (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2bf17029a706ad6902a8a01a14e73183f94d7a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715217"
---
# <a name="field-object-ado"></a>Объект Field (ADO)


**Применимо к**: Access 2013, Office 2013

Представляет столбец данных с типом данных.

## <a name="remarks"></a>Замечания

Каждый объект **поля** соответствует столбца в [набора записей](recordset-object-ado.md). Задает или возвращает данные для текущей записи используйте свойство [Value](value-property-ado.md) объектов **полей** . В зависимости от функциональности предоставляет поставщик, некоторые коллекции методов, или свойства объекта **поля** могут быть недоступны.

С помощью семейства сайтов, методы и свойства объекта **поля** сделайте следующее:

  - Возвращает имя поля с помощью свойства [Name](name-property-ado.md) .

  - Просмотр или изменение данных в поле с помощью свойства **Value** . **Значение** является свойством по умолчанию объекта **поля** .

  - Возвращает основные характеристики поля со свойствами [типа](type-property-ado.md), [точность](precision-property-ado.md)и [NumericScale](numericscale-property-ado.md) .

  - Возвращает объявленные размер поля со свойством [DefinedSize](definedsize-property-ado.md) .

  - В этом поле со свойством [ActualSize](actualsize-property-ado.md) возвращает фактический размер данных.

  - Определите, какие функциональные возможности поддерживаются для данного поля со свойством [атрибуты](attributes-property-ado.md) и [Свойства](properties-collection-ado.md) коллекции.

  - Работа с элементами управления значения полей, содержащие данные длинный двоичные или много символов с помощью методов [AppendChunk](appendchunk-method-ado.md) и [GetChunk](getchunk-method-ado.md) .

  - Если поставщик поддерживает пакетные обновления, разрешения несоответствий в значения полей во время обновление пакета с помощью свойства [OriginalValue](originalvalue-property-ado.md) и [UnderlyingValue](underlyingvalue-property-ado.md) .

Все свойства метаданных (**имя**, **Тип**, **DefinedSize**, **точности**и **NumericScale**) доступны перед открытием объекта **поля** **набора записей**. Задание их в это время полезно для динамического создания форм.

