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

## <a name="remarks"></a>Заметки

Данные в **ячейках извлекаются** с помощью прямого доступа, подобного массиву. Вы можете "развернуть" определенный член, чтобы получить данные об этом члене. Например, следующий код возвращает заголовок первого члена в первой позиции на первой оси ячейки cst:

`cst.Axes(0).Positions(0).Members(0).Caption`

В ячейках нет представления о текущей ячейке. Вместо этого свойство [Item](item-property-ado-md-cellset.md) извлекает определенный объект [Cell](cell-object-ado-md.md) из ячейки. Аргументы свойства **Item** определяют извлекаемую ячейку. Можно указать уникальное порядковое значение ячейки. Вы также можете получить ячейки, используя их номера позиции вдоль каждой оси ячеек. Дополнительные сведения о том, как получить ячейки, см. в [свойстве Item.](item-property-ado-md-cellset.md)

С помощью коллекций, методов и свойств объекта **Cellset** можно сделать следующее:

  - Связывание открытого подключения с объектом **Cellset** путем установки его свойства [ActiveConnection.](activeconnection-property-ado-md.md)

  - Выполнение и извлечение результатов многомерного запроса с помощью метода [Open.](open-method-ado-md.md)

  - **Извлечение ячейки** из **ячейки с** [свойством Item.](item-property-ado-md-cellset.md)

  - Возвращает [объекты Axis,](axis-object-ado-md.md) которые определяют **ячейки с** [коллекцией Axes.](axes-collection-ado-md.md)

  - Извлекать сведения об измерениях, используемых  для фильтрации данных в ячейках с помощью свойства [FilterAxis.](filteraxis-property-ado-md.md)

  - Возвращает или указывает запрос, используемый для определения **ячейки с** помощью [свойства Source.](source-property-ado-md.md)

  - Возвращает текущее состояние **cellset** (открытие, закрытое, выполнение или подключение) со [свойством State.](state-property-ado-md.md)

  - Закроем **открытый ячейки** с помощью метода [Close.](close-method-ado-md.md)

  - Извлечение сведений о **cellset** для конкретного поставщика со стандартной коллекцией [свойств](properties-collection-ado.md) ADO.

