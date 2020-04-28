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

## <a name="remarks"></a>Примечания

Многие поставщики поддерживают параметризованные команды. Это команды, в которых нужное действие определено один раз, но переменные (или параметры) используются для изменения некоторых сведений о команде. Например, инструкция SQL SELECT может использовать параметр для определения условия соответствия предложения WHERE, а другое — для определения имени столбца для предложения SORT BY.

Объект **Parameter** представляет параметры, связанные с параметризованными запросами, а также аргументы in/out и возвращаемые значения хранимых процедур. В зависимости от функциональных возможностей поставщика некоторые коллекции, методы или свойства объекта **Parameter** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Parameter** можно выполнить следующие действия:

  - Задайте или верните имя параметра с помощью свойства [Name](name-property-ado.md) .

  - Задайте или возвратите значение параметра со свойством [value](value-property-ado.md) . **Value** является свойством по умолчанию для объекта **Parameter** .

  - Задайте или возвращает характеристики параметров с помощью свойств [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [size](size-property-ado.md)и [Type](type-property-ado.md) .

  - Передача длинных двоичных или символьных данных в параметр с помощью метода [AppendChunk](appendchunk-method-ado.md) .

  - Доступ к атрибутам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .

Если вы знаете имена и свойства параметров, связанных с хранимой процедурой или параметризованным запросом, который вы хотите вызвать, можно использовать метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Parameter** с соответствующими параметрами свойства и использовать метод [append](append-method-ado.md) , чтобы добавить их в коллекцию [Parameters](parameters-collection-ado.md) . Это позволяет задавать и возвращать значения параметров, не выполняя вызов метода [Refresh](refresh-method-ado.md) коллекции **Parameters** для получения сведений о параметрах от поставщика, потенциально требовательных к ресурсам операций.

