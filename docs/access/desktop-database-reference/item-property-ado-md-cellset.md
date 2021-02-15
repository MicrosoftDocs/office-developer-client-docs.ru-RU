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
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="b7ae2-102">Свойство Item (Cellset в ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b7ae2-102">Item property (ADO MD Cellset)</span></span>

<span data-ttu-id="b7ae2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7ae2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7ae2-104">Извлекает ячейку из ячейки с помощью ее координат.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ae2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7ae2-105">Syntax</span></span>

<span data-ttu-id="b7ae2-106">Set *Cell*  =  *Cellset*. Item (*Positions*)</span><span class="sxs-lookup"><span data-stu-id="b7ae2-106">Set *Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="b7ae2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7ae2-107">Parameters</span></span>

|<span data-ttu-id="b7ae2-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b7ae2-108">Parameter</span></span>|<span data-ttu-id="b7ae2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b7ae2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b7ae2-110">*Positions*</span><span class="sxs-lookup"><span data-stu-id="b7ae2-110">*Positions*</span></span> |<span data-ttu-id="b7ae2-111">Массив **значений Variant,** однозначно определяя ячейку.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-111">A **Variant array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="b7ae2-112">*Позиции могут* быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="b7ae2-112">*Positions* can be one of the following:</span></span><br/><br/><span data-ttu-id="b7ae2-113">- Массив номеров позиции</span><span class="sxs-lookup"><span data-stu-id="b7ae2-113">- An array of position numbers</span></span><br/><span data-ttu-id="b7ae2-114">- Массив имен членов</span><span class="sxs-lookup"><span data-stu-id="b7ae2-114">- An array of member names</span></span><br/><span data-ttu-id="b7ae2-115">- Порядковая позиция</span><span class="sxs-lookup"><span data-stu-id="b7ae2-115">- The ordinal position</span></span> |

## <a name="remarks"></a><span data-ttu-id="b7ae2-116">Заметки</span><span class="sxs-lookup"><span data-stu-id="b7ae2-116">Remarks</span></span>

<span data-ttu-id="b7ae2-117">Используйте свойство **Item** для возврата объекта [Cell](cell-object-ado-md.md) в [объекте Cellset.](cellset-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="b7ae2-117">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="b7ae2-118">Если **свойству Item** не удается найти ячейку, соответствующую аргументу *Positions,* возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-118">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="b7ae2-119">Свойство **Item** является свойством по умолчанию для объекта **Cellset.**</span><span class="sxs-lookup"><span data-stu-id="b7ae2-119">The **Item** property is the default property for the **Cellset** object.</span></span> <span data-ttu-id="b7ae2-120">Следующие синтаксис-формы являются взаимозаменяемыми:</span><span class="sxs-lookup"><span data-stu-id="b7ae2-120">The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="b7ae2-121">Аргумент *Positions* указывает возвращаемую ячейку.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-121">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="b7ae2-122">Ячейку можно указать по порядковому положению или по позиции вдоль каждой оси.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-122">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="b7ae2-123">При указании ячейки по позиции вдоль каждой оси можно указать числовую позицию или имена членов для каждой позиции.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-123">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="b7ae2-124">Порядковая позиция — это число, уникальным образом идентифицирует одну ячейку в **cellset.**</span><span class="sxs-lookup"><span data-stu-id="b7ae2-124">The ordinal position is a number that uniquely identifies one cell within the **Cellset**.</span></span> <span data-ttu-id="b7ae2-125">Концептуально ячейки нумеруются в  ячейках, как если бы ячейки были массивом *p-dimensional,* *где p* — это число осей. </span><span class="sxs-lookup"><span data-stu-id="b7ae2-125">Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes.</span></span> <span data-ttu-id="b7ae2-126">Ячейки адресованы в порядке с основными строками.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-126">Cells are addressed in row-major order.</span></span>

<span data-ttu-id="b7ae2-127">Если имена членов передаются в качестве строк в **item,** они должны быть указаны в порядке увеличения числимого идентификатора оси.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-127">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers.</span></span> <span data-ttu-id="b7ae2-128">Внутри оси члены должны быть указаны в порядке увеличения вложенности измерений, то есть на первое место идет член внешнего измерения, за которым следуют члены внутренних измерений.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-128">Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions.</span></span> <span data-ttu-id="b7ae2-129">Каждое измерение должно быть представлено отдельной строкой, а список строк членов должен разделяться запятой.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-129">Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="b7ae2-130">Сбор ячеек по имени участника может не поддерживаться поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-130">Retrieving cells by member name may not be supported by your data provider.</span></span> <span data-ttu-id="b7ae2-131">Дополнительные сведения см. в документации к поставщику.</span><span class="sxs-lookup"><span data-stu-id="b7ae2-131">See the documentation for your provider for more information.</span></span>


