---
title: Свойство Item (ADO MD Cellset)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fdf405ab5cd59e7ab4268e2fea870272836fb164
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949609"
---
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="e5ab7-102">Свойство Item (ADO MD Cellset)</span><span class="sxs-lookup"><span data-stu-id="e5ab7-102">Item property (ADO MD Cellset)</span></span>

<span data-ttu-id="e5ab7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5ab7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5ab7-104">Получает ячейки из набора координат ячеек.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ab7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5ab7-105">Syntax</span></span>

<span data-ttu-id="e5ab7-106">Установить в*ячейке* = *ячеек*. Элемент (*положения*)</span><span class="sxs-lookup"><span data-stu-id="e5ab7-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e5ab7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5ab7-107">Parameters</span></span>

|<span data-ttu-id="e5ab7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="e5ab7-108">Parameter</span></span>|<span data-ttu-id="e5ab7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e5ab7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e5ab7-110">*Положения*</span><span class="sxs-lookup"><span data-stu-id="e5ab7-110">*Positions*</span></span> |<span data-ttu-id="e5ab7-111">**Вариантный массив** значений, которые однозначно указать ячейки.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-111">A **Variant array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="e5ab7-112">*Положения* может иметь одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="e5ab7-112">*Positions* can be one of the following:</span></span><br/><br/><span data-ttu-id="e5ab7-113">-Массив положение чисел</span><span class="sxs-lookup"><span data-stu-id="e5ab7-113">- An array of position numbers</span></span><br/><span data-ttu-id="e5ab7-114">-Массив имена элементов</span><span class="sxs-lookup"><span data-stu-id="e5ab7-114">- An array of member names</span></span><br/><span data-ttu-id="e5ab7-115">-Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="e5ab7-115">- The ordinal position</span></span> |

## <a name="remarks"></a><span data-ttu-id="e5ab7-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5ab7-116">Remarks</span></span>

<span data-ttu-id="e5ab7-117">Используйте свойство **Item** возвращает объект [ячейки](cell-object-ado-md.md) в объекте [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ab7-117">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="e5ab7-118">Если свойство **Item** не удается найти ячейки, соответствующий аргумент *положения* , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-118">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="e5ab7-119">Свойство **Item** является свойством по умолчанию для объекта **ячеек** .</span><span class="sxs-lookup"><span data-stu-id="e5ab7-119">The **Item** property is the default property for the **Cellset** object.</span></span> <span data-ttu-id="e5ab7-120">Следующие формы синтаксиса являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-120">The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="e5ab7-121">Аргумент *положения* указывает, какие ячейки для возврата.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-121">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="e5ab7-122">Можно указать ячейку с порядковый номер или положение каждой оси.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-122">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="e5ab7-123">При указании ячейки по позиции каждой оси, можно указать числовое значение положения или имена элементов для каждой позиции.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-123">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="e5ab7-124">Порядковый номер — это число, однозначно идентифицирующее одну ячейку в пределах **ячеек**.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-124">The ordinal position is a number that uniquely identifies one cell within the **Cellset**.</span></span> <span data-ttu-id="e5ab7-125">Концептуально ячеек нумеруются в **набор ячеек** , как будто **ячеек** *p*-двумерного массива array, где *p* — это число осей.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-125">Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes.</span></span> <span data-ttu-id="e5ab7-126">Описываются ячеек строкам.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-126">Cells are addressed in row-major order.</span></span>

<span data-ttu-id="e5ab7-127">Если имена элементов передаются как строки для **элементов**, элементы должны быть перечислены в порядке возрастания их идентификаторы числовой оси.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-127">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers.</span></span> <span data-ttu-id="e5ab7-128">Внутри оси, по возрастанию вложенности измерения должны быть перечислены члены, то есть элемент измерения внешней идет первой, следуют элементы внутреннего измерений.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-128">Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions.</span></span> <span data-ttu-id="e5ab7-129">Каждого измерения должны быть представлены в отдельную строку и список строк член должен быть, разделив их запятыми.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-129">Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="e5ab7-130">Получение ячейки с именем члена может не поддерживаться поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-130">Retrieving cells by member name may not be supported by your data provider.</span></span> <span data-ttu-id="e5ab7-131">Обратитесь к документации вашего поставщика для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="e5ab7-131">See the documentation for your provider for more information.</span></span>


