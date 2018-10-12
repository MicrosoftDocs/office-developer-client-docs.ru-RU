---
title: Parameter Object (ADO)
TOCTitle: Parameter Object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7667828d2ebfdc554a7120bf495374bc50e51cfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480589"
---
# <a name="parameter-object-ado"></a>Parameter Object (ADO)


**Применимо к**: Access 2013 | Office 2013

Представляет параметр или аргумент, связанной с объектом [команды](command-object-ado.md) на основе параметризованный запрос или хранимую процедуру.

## <a name="remarks"></a>Замечания

Многие поставщики поддерживают параметризованные команды. Ниже приведены команды, в которых нужное действие определяется один раз, но переменные (или параметров) используются для изменения некоторые сведения команды. Например источников данных можно использовать параметр для определения условий соответствия предложение WHERE, и другая, чтобы определить имя столбца для СОРТИРОВКИ BY.

Объекты **параметров** представляют параметры, связанные с параметризованные запросы или/out аргументы и возвращаемые значения хранимые процедуры. В зависимости от функциональности поставщика некоторые семейств сайтов, методы и свойства **параметра** объект не может быть доступно.

С помощью семейства сайтов, методы и свойства объекта **параметра** сделайте следующее:

  - Установить или возвращает имя параметра с помощью свойства [Name](name-property-ado.md) .

  - Установить или возвращаемое значение параметра с помощью свойства [Value](value-property-ado.md) . **Значение** является свойством по умолчанию объекта **параметров** .

  - Задать или вернуть характеристики параметра с [атрибутами](attributes-property-ado.md), [направление](direction-property-ado.md), [точность](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [размер](size-property-ado.md)и [Тип](type-property-ado.md) свойства.

  - Передайте длинный двоичный или символ данных параметр с помощью метода [AppendChunk](appendchunk-method-ado.md) .

  - Атрибуты поставщика доступа с набором [свойств](properties-collection-ado.md) .

Если знать имена, свойства параметров, связанных с хранимую процедуру или параметризованный запрос, необходимо вызвать метод [CreateParameter](createparameter-method-ado.md) можно использовать для создания объектов **параметров** с соответствующими параметрами свойств и метод [Append](append-method-ado.md) используется для добавления их в коллекцию [параметров](parameters-collection-ado.md) . Это позволяет задать и возвращаемые значения параметра без необходимости для вызова метода [обновления](refresh-method-ado.md) на коллекцию **параметров** для получения сведений о параметрах от поставщика, потенциально ресурсоемких операции.
