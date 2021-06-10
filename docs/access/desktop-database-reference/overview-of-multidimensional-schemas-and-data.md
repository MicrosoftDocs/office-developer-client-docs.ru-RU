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

## <a name="understanding-multidimensional-schemas"></a>Понимание многомерных схем

Центральным объектом метаданных в ADO MD является *куб,* состоящий из структурированного набора связанных измерений, иерархий, уровней и участников.

Измерение *—* это независимая категория данных из многомерной базы данных, полученная из бизнес-сущностями. Измерение обычно содержит элементы, которые будут использоваться в качестве критериев запроса для мер базы данных.

Иерархия *—* это путь агрегации измерения. Измерение может иметь несколько уровней детализации, которые имеют родительские и детские отношения. Иерархия определяет, как эти уровни связаны.

Уровень *—* это шаг агрегации в иерархии. Для размеров с несколькими уровнями информации каждый слой является уровнем.

Член *—* это элемент данных в измерении. Как правило, вы создаете подпись или описываете меру базы данных с помощью участников.

Куби представлены [объектами CubeDef](cubedef-object-ado-md.md) в ADO MD. Размеры, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensions

Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных. Как правило, каждое измерение является независимой точкой входа или механизмом выбора данных.

Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products и Measures. Измерение Measures содержит фактические значения данных о продажах, в то время как другие измерения представляют способы классификации и группы значений данных о продажах.

Измерение Географии имеет следующий набор участников:

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

В примере измерения географии, изображенном на предыдущем рисунке, каждое поле представляет уровень иерархии.

Каждый уровень имеет набор участников:

  - Мир = {All}

  - Континенты = {Северная Америка, Европа}

  - Страны = {Канада, США, Великобритания, Германия}

  - Регионы = {Canada-East, Canada-West, USA-NE, USA-NW, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}

  - Города = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}

## <a name="members"></a>"Участники"

Члены на уровне листа иерархии не имеют детей, а члены на корневом уровне не имеют родителей. Все остальные члены имеют по крайней мере одного родителя и по крайней мере одного ребенка. Например, частичный обход дерева иерархии в измерении География дает следующие отношения между родителем и ребенком:

- {All} (родитель) {Европа, Северная Америка}
- {Северная Америка} (родитель) {Канада, США}
- {USA} (родитель) {USA-NE, USA-NW, USA-SE, USA-SW}
- {USA-NW} (родитель) {Boise, Seattle}

Участники могут быть консолидированы по одной или несколько иерархий на одно измерение.

В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter. Таким образом, иерархия не должна включать все члены измерения.

## <a name="understanding-multidimensional-schemas"></a>Понимание многомерных схем

Центральным объектом метаданных в ADO MD является *куб,* состоящий из структурированного набора связанных измерений, иерархий, уровней и участников.

Измерение *—* это независимая категория данных из многомерной базы данных, полученная из бизнес-сущностями. Измерение обычно содержит элементы, которые будут использоваться в качестве критериев запроса для мер базы данных.

Иерархия *—* это путь агрегации измерения. Измерение может иметь несколько уровней детализации, которые имеют родительские и детские отношения. Иерархия определяет, как эти уровни связаны.

Уровень *—* это шаг агрегации в иерархии. Для размеров с несколькими уровнями информации каждый слой является уровнем.

Член *—* это элемент данных в измерении. Как правило, вы создаете подпись или описываете меру базы данных с помощью участников.

Куби представлены [объектами CubeDef](cubedef-object-ado-md.md) в ADO MD. Размеры, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensions

Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных. Как правило, каждое измерение является независимой точкой входа или механизмом выбора данных.

Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products и Measures. Измерение Measures содержит фактические значения данных о продажах, в то время как другие измерения представляют способы классификации и группы значений данных о продажах.

Измерение Географии имеет следующий набор участников:

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

В примере измерения географии, изображенном на предыдущем рисунке, каждое поле представляет уровень иерархии.

Каждый уровень имеет набор участников:

- Мир = {All}

- Континенты = {Северная Америка, Европа}

- Страны = {Канада, США, Великобритания, Германия}

- Регионы = {Canada-East, Canada-West, USA-NE, USA-NW, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}

- Города = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}

## <a name="members"></a>"Участники"

Члены на уровне листа иерархии не имеют детей, а члены на корневом уровне не имеют родителей. Все остальные члены имеют по крайней мере одного родителя и по крайней мере одного ребенка. Например, частичный обход дерева иерархии в измерении География дает следующие отношения между родителем и ребенком:

- {All} (родитель) {Европа, Северная Америка}

- {Северная Америка} (родитель) {Канада, США}

- {USA} (родитель) {USA-NE, USA-NW, USA-SE, USA-SW}

- {USA-NW} (родитель) {Boise, Seattle}

Участники могут быть консолидированы по одной или несколько иерархий на одно измерение.

В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter. Таким образом, иерархия не должна включать все члены измерения.

