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
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="f1918-102">Свойство Item (Cellset в ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f1918-102">Item property (ADO MD Cellset)</span></span>

<span data-ttu-id="f1918-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1918-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1918-104">Извлекает ячейку из ячейки с помощью ее координат.</span><span class="sxs-lookup"><span data-stu-id="f1918-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1918-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1918-105">Syntax</span></span>

<span data-ttu-id="f1918-106">Установите  =  *ячейки ячейки*. Item *(Positions)*</span><span class="sxs-lookup"><span data-stu-id="f1918-106">Set *Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f1918-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1918-107">Parameters</span></span>

|<span data-ttu-id="f1918-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f1918-108">Parameter</span></span>|<span data-ttu-id="f1918-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f1918-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f1918-110">*Positions*</span><span class="sxs-lookup"><span data-stu-id="f1918-110">*Positions*</span></span> |<span data-ttu-id="f1918-111">Массив **значений Variant,** который однозначно указывает ячейку.</span><span class="sxs-lookup"><span data-stu-id="f1918-111">A **Variant array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="f1918-112">*Позиции могут* быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="f1918-112">*Positions* can be one of the following:</span></span><br/><br/><span data-ttu-id="f1918-113">- Массив номеров позиций</span><span class="sxs-lookup"><span data-stu-id="f1918-113">- An array of position numbers</span></span><br/><span data-ttu-id="f1918-114">- Массив имен членов</span><span class="sxs-lookup"><span data-stu-id="f1918-114">- An array of member names</span></span><br/><span data-ttu-id="f1918-115">- Ordinal position</span><span class="sxs-lookup"><span data-stu-id="f1918-115">- The ordinal position</span></span> |

## <a name="remarks"></a><span data-ttu-id="f1918-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1918-116">Remarks</span></span>

<span data-ttu-id="f1918-117">Используйте свойство **Item** для возвращения объекта [Cell](cell-object-ado-md.md) в [объект Cellset.](cellset-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="f1918-117">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="f1918-118">Если свойство **Item** не может найти ячейку, соответствующую аргументу *Positions,* возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1918-118">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="f1918-119">Свойство **Item** — это свойство по умолчанию для объекта **Cellset.**</span><span class="sxs-lookup"><span data-stu-id="f1918-119">The **Item** property is the default property for the **Cellset** object.</span></span> <span data-ttu-id="f1918-120">Следующие формы синтаксиса являются взаимозаменяемыми:</span><span class="sxs-lookup"><span data-stu-id="f1918-120">The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="f1918-121">Аргумент *Positions* указывает, какую ячейку возвращать.</span><span class="sxs-lookup"><span data-stu-id="f1918-121">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="f1918-122">Ячейку можно указать по координатной позиции или по положению вдоль каждой оси.</span><span class="sxs-lookup"><span data-stu-id="f1918-122">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="f1918-123">При указании ячейки по позициям вдоль каждой оси можно указать численное значение позиции или имена участников для каждой позиции.</span><span class="sxs-lookup"><span data-stu-id="f1918-123">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="f1918-124">Координатная позиция — это число, которое уникально определяет одну ячейку в **Cellset.**</span><span class="sxs-lookup"><span data-stu-id="f1918-124">The ordinal position is a number that uniquely identifies one cell within the **Cellset**.</span></span> <span data-ttu-id="f1918-125">Концептуально ячейки нумеруются в  **ячейках** так, как если бы ячейки были *p-мерным* массивом, где *p* — это число осей.</span><span class="sxs-lookup"><span data-stu-id="f1918-125">Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes.</span></span> <span data-ttu-id="f1918-126">Ячейки адресованы в порядке row-major.</span><span class="sxs-lookup"><span data-stu-id="f1918-126">Cells are addressed in row-major order.</span></span>

<span data-ttu-id="f1918-127">Если имена участников передаются в качестве строк **в Item,** их необходимо перечислены в порядке увеличения числимого идентификатора оси.</span><span class="sxs-lookup"><span data-stu-id="f1918-127">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers.</span></span> <span data-ttu-id="f1918-128">В оси участники должны быть указаны в порядке вложения измерений, то есть на первое место выходит член внешнего измерения, за которым следуют члены внутренних измерений.</span><span class="sxs-lookup"><span data-stu-id="f1918-128">Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions.</span></span> <span data-ttu-id="f1918-129">Каждое измерение должно быть представлено отдельной строкой, а список строк участников должен быть разделен запятой.</span><span class="sxs-lookup"><span data-stu-id="f1918-129">Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="f1918-130">Сбор ячеек по имени участника может не поддерживаться поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="f1918-130">Retrieving cells by member name may not be supported by your data provider.</span></span> <span data-ttu-id="f1918-131">Дополнительные сведения см. в документации для поставщика.</span><span class="sxs-lookup"><span data-stu-id="f1918-131">See the documentation for your provider for more information.</span></span>


