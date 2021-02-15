---
title: Обзор многомерных схем и данных
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288156"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>Обзор многомерных схем и данных

**Область применения**: Access 2013, Office 2013

## <a name="understanding-multidimensional-schemas"></a>Understanding Multidimensional Schemas

Центральный объект метаданных в ADO MD — это *куб,* который состоит из структурированного набора связанных измерений, иерархий, уровней и членов.

Измерение *—* это независимая категория данных из многомерной базы данных, производная от бизнес-сущностями. Измерение обычно содержит элементы, используемые в качестве критериев запроса для мер базы данных.

Иерархия *—* это путь агрегации измерения. Измерение может иметь несколько уровней детализации с родительскими и родительскими отношениями. Иерархия определяет, как эти уровни связаны.

Уровень *—* это этап агрегации в иерархии. Для измерений с несколькими уровнями информации каждый уровень является уровнем.

Элемент *—* это элемент данных в измерении. Как правило, вы создаете заголовок или описываете меру базы данных с помощью членов.

Кубы представлены объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD. Измерения, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md)

## <a name="dimensions"></a>Dimensions

Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных. Как правило, каждое измерение является независимой точкой входа или механизмом для выбора данных.

Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products, and Measures. Измерение "Меры" содержит фактические значения данных о продажах, а другие измерения представляют способы классификации и группировки значений данных о продажах.

Измерение "География" имеет следующий набор членов:

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hierarchies

Иерархии определяют способы,которыми можно "свернуть" или сгруппить уровни измерения. Измерение может иметь несколько иерархий.

## <a name="levels"></a>Levels

В примере измерения "География", изображенном на предыдущем рисунке, каждое поле представляет уровень в иерархии.

Каждый уровень имеет набор членов, как поется ниже.

  - The World = {All}

  - Континенты = {Северная Америка, Европа}

  - Страны = {Канада, США, Соединенное Королевство, Германия}

  - Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}

  - Города = {Ottawa, Vancouver, Vancouver, Vancouver, Seattle, Boise, Los Seattle Seattle, Los Seattle, Shreveport, Meve, Meve, Los, New York, London, Dover, Seattleh, Cardiff, Pembroke, Losfast, London, Hamburg, Hamburg, Stuttgart}

## <a name="members"></a>"Участники"

Члены на конечном уровне иерархии не имеют потомка, а члены на корневом уровне не имеют родительских. Все остальные члены имеют по крайней мере один родительский и по крайней мере один потомок. Например, частичный обход дерева иерархии в измерении "География" дает следующие родительские и родительские отношения:

- {All} (родительский) {Europe, North America}
- {Северная Америка} (родительский) {Канада, США}
- {USA} (родительский) {USA-NE, USA-NW, USA-SE, USA-SW}
- {USA-NW} (родительский) {Boise, Seattle}

Члены могут быть объединены в одну или несколько иерархий на измерение.

В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter иерархии. Таким образом, иерархия не должна включать все члены измерения.

## <a name="understanding-multidimensional-schemas"></a>Understanding Multidimensional Schemas

Центральный объект метаданных в ADO MD — это *куб,* который состоит из структурированного набора связанных измерений, иерархий, уровней и членов.

Измерение *—* это независимая категория данных из многомерной базы данных, производная от бизнес-сущностями. Измерение обычно содержит элементы, используемые в качестве критериев запроса для мер базы данных.

Иерархия *—* это путь агрегации измерения. Измерение может иметь несколько уровней детализации с родительскими и родительскими отношениями. Иерархия определяет, как эти уровни связаны.

Уровень *—* это этап агрегации в иерархии. Для измерений с несколькими уровнями информации каждый уровень является уровнем.

Элемент *—* это элемент данных в измерении. Как правило, вы создаете заголовок или описываете меру базы данных с помощью членов.

Кубы представлены объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD. Измерения, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md)

## <a name="dimensions"></a>Dimensions

Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных. Как правило, каждое измерение является независимой точкой входа или механизмом для выбора данных.

Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products, and Measures. Измерение "Меры" содержит фактические значения данных о продажах, а другие измерения представляют способы классификации и группировки значений данных о продажах.

Измерение "География" имеет следующий набор членов:

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hierarchies

Иерархии определяют способы,которыми можно "свернуть" или сгруппить уровни измерения. Измерение может иметь несколько иерархий.

## <a name="levels"></a>Levels

В примере измерения "География", изображенном на предыдущем рисунке, каждое поле представляет уровень в иерархии.

Каждый уровень имеет набор членов, как поется ниже.

- The World = {All}

- Континенты = {Северная Америка, Европа}

- Страны = {Канада, США, Соединенное Королевство, Германия}

- Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}

- Города = {Ottawa, Vancouver, Vancouver, Vancouver, Seattle, Boise, Los Seattle Seattle, Los Seattle, Shreveport, Meve, Meve, Los, New York, London, Dover, Seattleh, Cardiff, Pembroke, Losfast, London, Hamburg, Hamburg, Stuttgart}

## <a name="members"></a>"Участники"

Члены на конечном уровне иерархии не имеют потомка, а члены на корневом уровне не имеют родительских. Все остальные члены имеют по крайней мере один родительский и по крайней мере один потомок. Например, частичный обход дерева иерархии в измерении "География" дает следующие родительские и родительские отношения:

- {All} (родительский) {Europe, North America}

- {Северная Америка} (родительский) {Канада, США}

- {USA} (родительский) {USA-NE, USA-NW, USA-SE, USA-SW}

- {USA-NW} (родительский) {Boise, Seattle}

Члены могут быть объединены в одну или несколько иерархий на измерение.

В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter иерархии. Таким образом, иерархия не должна включать все члены измерения.

