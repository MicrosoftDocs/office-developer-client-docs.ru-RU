---
title: Объект Cellset (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296516"
---
# <a name="cellset-object-ado-md"></a>Объект Cellset (ADO MD)

**Область применения**: Access 2013, Office 2013

Представляет результаты многомерного запроса. Это коллекция ячеек, выбранных из кубов или других ячеек.

## <a name="remarks"></a>Примечания

Данные в **ячейках** извлекаются с помощью прямого, массивного доступа. Для получения данных об этом члене можно "сверлить" определенный член. Например, в следующем коде возвращается подпись первого участника в первой позиции на первой оси ячейки cST:

`cst.Axes(0).Positions(0).Members(0).Caption`

В ячейке нет понятия текущей ячейки. Вместо этого свойство [Item](item-property-ado-md-cellset.md) извлекает определенный объект [Cell](cell-object-ado-md.md) из ячейки. Аргументы свойства **Item** определяют, какая ячейка извлекается. Вы можете указать уникальное ordinal значение ячейки. Вы также можете получить ячейки с помощью их номеров положения вдоль каждой оси ячейки. Дополнительные сведения о том, как получить ячейки, см. в статье [Свойство Item.](item-property-ado-md-cellset.md)

С помощью коллекций, методов и свойств объекта **Cellset** можно сделать следующее:

  - Связать открытое подключение с объектом **Cellset,** установив его свойство [ActiveConnection.](activeconnection-property-ado-md.md)

  - Выполнение и извлечение результатов многомерного запроса с помощью метода [Open.](open-method-ado-md.md)

  - **Извлечение ячейки** из **ячейки с** [свойством Item.](item-property-ado-md-cellset.md)

  - Верни [объекты Axis,](axis-object-ado-md.md) которые определяют **ячейки с** [коллекцией Axes.](axes-collection-ado-md.md)

  - Извлечение сведений о измерениях, используемых для фильтрации данных в **ячейках** с помощью [свойства FilterAxis.](filteraxis-property-ado-md.md)

  - Возвращайте или укажите запрос, используемый для определения **ячейки с** [свойством Source.](source-property-ado-md.md)

  - Возвращаем текущее состояние **Cellset** (открытое, закрытое, выполнение или подключение) с [свойством состояния.](state-property-ado-md.md)

  - Закрой **открытый ячейки** методом [Close.](close-method-ado-md.md)

  - Извлечение сведений, определенных для поставщика, о **ячейках в** стандартной коллекции свойств [ADO.](properties-collection-ado.md)

