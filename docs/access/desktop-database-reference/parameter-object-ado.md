---
title: Объект Parameter (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6f3acd4af280f30706e35eb7ecda1dee11aa7d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288079"
---
# <a name="parameter-object-ado"></a>Объект Parameter (ADO)


**Область применения**: Access 2013, Office 2013

Представляет параметр или аргумент, связанный с объектом [Command](command-object-ado.md) на основе параметризованного запроса или хранимой процедуры.

## <a name="remarks"></a>Заметки

Многие поставщики поддерживают параметризованные команды. Это команды, в которых нужное действие определяется один раз, но переменные (или параметры) используются для изменения некоторых сведений о команде. Например, SQL SELECT может использовать параметр для определения критериев соответствия предложению WHERE, а другой — для определения имени столбца для предложения SORT BY.

 Объекты-параметры представляют параметры, связанные с параметризированными запросами, а также аргументы и возвращаемого значения хранимых процедур. В зависимости от функциональности поставщика некоторые коллекции, методы или свойства объекта **Parameter** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Parameter** можно сделать следующее:

  - Задан или возвращено имя параметра со [свойством Name.](name-property-ado.md)

  - Установите или вернетесь значение параметра со [свойством Value.](value-property-ado.md) **Значение** является свойством по умолчанию объекта **Parameter.**

  - Заданы или возвращены характеристики параметра со свойствами [Attributes,](attributes-property-ado.md) [Direction,](direction-property-ado.md) [Precision,](precision-property-ado.md) [NumericScale,](numericscale-property-ado.md) [Size](size-property-ado.md)и [Type.](type-property-ado.md)

  - Передав длинные двоичные или символьные данные в параметр с помощью метода [AppendChunk.](appendchunk-method-ado.md)

  - Доступ к атрибутам поставщика с помощью коллекции [Properties.](properties-collection-ado.md)

Если вы знаете имена и свойства параметров, связанных с хранимой процедурой или параметризированным запросом, который требуется вызвать, можно использовать метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Parameter** с соответствующими параметрами свойств и с помощью метода [Append](append-method-ado.md) добавить их в коллекцию [Parameters.](parameters-collection-ado.md) Это позволяет устанавливать и возвращать значения параметров без вызова метода [Refresh](refresh-method-ado.md) в коллекции **Parameters** для получения сведений о параметрах от поставщика, что может быть ресурсоемкой операцией.

