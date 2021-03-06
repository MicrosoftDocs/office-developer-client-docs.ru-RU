---
title: Свойство Item (Cellset в ADO MD)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99f381ad2f38dc7d2c467ed1e40e4084032006d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290869"
---
# <a name="item-property-ado-md-cellset"></a>Свойство Item (Cellset в ADO MD)

**Область применения**: Access 2013, Office 2013

Извлекает ячейку из ячейки с помощью ее координат.

## <a name="syntax"></a>Синтаксис

Установите  =  *ячейки ячейки*. Item *(Positions)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Positions* |Массив **значений Variant,** который однозначно указывает ячейку. *Позиции могут* быть одним из следующих:<br/><br/>- Массив номеров позиций<br/>- Массив имен членов<br/>- Ordinal position |

## <a name="remarks"></a>Примечания

Используйте свойство **Item** для возвращения объекта [Cell](cell-object-ado-md.md) в [объект Cellset.](cellset-object-ado-md.md) Если свойство **Item** не может найти ячейку, соответствующую аргументу *Positions,* возникает ошибка.

Свойство **Item** — это свойство по умолчанию для объекта **Cellset.** Следующие формы синтаксиса являются взаимозаменяемыми:

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

Аргумент *Positions* указывает, какую ячейку возвращать. Ячейку можно указать по координатной позиции или по положению вдоль каждой оси. При указании ячейки по позициям вдоль каждой оси можно указать численное значение позиции или имена участников для каждой позиции.

Координатная позиция — это число, которое уникально определяет одну ячейку в **Cellset.** Концептуально ячейки нумеруются в  **ячейках** так, как если бы ячейки были *p-мерным* массивом, где *p* — это число осей. Ячейки адресованы в порядке row-major.

Если имена участников передаются в качестве строк **в Item,** их необходимо перечислены в порядке увеличения числимого идентификатора оси. В оси участники должны быть указаны в порядке вложения измерений, то есть на первое место выходит член внешнего измерения, за которым следуют члены внутренних измерений. Каждое измерение должно быть представлено отдельной строкой, а список строк участников должен быть разделен запятой.


> [!NOTE]
> Сбор ячеек по имени участника может не поддерживаться поставщиком данных. Дополнительные сведения см. в документации для поставщика.


