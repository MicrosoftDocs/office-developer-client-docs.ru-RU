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
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="5f402-102">Свойство Item (Cellset в ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5f402-102">Item property (ADO MD Cellset)</span></span>

<span data-ttu-id="5f402-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f402-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f402-104">Извлекает ячейку из элемента Cell с помощью ее координат.</span><span class="sxs-lookup"><span data-stu-id="5f402-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f402-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f402-105">Syntax</span></span>

<span data-ttu-id="5f402-106">Задайте набор*ячеек\*\*для ячейки.* =  Элемент (*Positions*)</span><span class="sxs-lookup"><span data-stu-id="5f402-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5f402-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f402-107">Parameters</span></span>

|<span data-ttu-id="5f402-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5f402-108">Parameter</span></span>|<span data-ttu-id="5f402-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5f402-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5f402-110">*Positions*</span><span class="sxs-lookup"><span data-stu-id="5f402-110">*Positions*</span></span> |<span data-ttu-id="5f402-111">**Массив вариантов** значений, который уникально задает ячейку.</span><span class="sxs-lookup"><span data-stu-id="5f402-111">A **Variant array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="5f402-112">*Положения* могут быть одним из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="5f402-112">*Positions* can be one of the following:</span></span><br/><br/><span data-ttu-id="5f402-113">— Массив номеров расположений</span><span class="sxs-lookup"><span data-stu-id="5f402-113">- An array of position numbers</span></span><br/><span data-ttu-id="5f402-114">— Массив имен элементов</span><span class="sxs-lookup"><span data-stu-id="5f402-114">- An array of member names</span></span><br/><span data-ttu-id="5f402-115">— Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="5f402-115">- The ordinal position</span></span> |

## <a name="remarks"></a><span data-ttu-id="5f402-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f402-116">Remarks</span></span>

<span data-ttu-id="5f402-117">Используйте свойство **Item** , чтобы возвратить объект [Cell](cell-object-ado-md.md) в объекте [Cell](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="5f402-117">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="5f402-118">Если свойству **Item** не удается найти ячейку, соответствующую аргументу *Positions* , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5f402-118">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="5f402-119">Свойство **Item** является свойством по умолчанию для объекта набором **ячеек** .</span><span class="sxs-lookup"><span data-stu-id="5f402-119">The **Item** property is the default property for the **Cellset** object.</span></span> <span data-ttu-id="5f402-120">Следующие синтаксические формы являются взаимозаменяемыми:</span><span class="sxs-lookup"><span data-stu-id="5f402-120">The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="5f402-121">Аргумент *Positions* указывает, какую ячейку нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="5f402-121">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="5f402-122">Вы можете указать ячейку по порядковому номеру или по позиции на каждой оси.</span><span class="sxs-lookup"><span data-stu-id="5f402-122">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="5f402-123">Указывая положение ячейки вдоль каждой оси, вы можете указать числовое значение позиции или имена элементов для каждой позиции.</span><span class="sxs-lookup"><span data-stu-id="5f402-123">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="5f402-124">Порядковый номер — это число, уникально идентифицирующее одну ячейку в наборе **ячеек**.</span><span class="sxs-lookup"><span data-stu-id="5f402-124">The ordinal position is a number that uniquely identifies one cell within the **Cellset**.</span></span> <span data-ttu-id="5f402-125">Как концептуально, ячейки пронумерованы *в наборе* **ячеек** , как если бы набор **ячеек** был одномерным массивом, где *p* — это количество осей.</span><span class="sxs-lookup"><span data-stu-id="5f402-125">Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes.</span></span> <span data-ttu-id="5f402-126">Ячейки направлены в основной порядок по строкам.</span><span class="sxs-lookup"><span data-stu-id="5f402-126">Cells are addressed in row-major order.</span></span>

<span data-ttu-id="5f402-127">Если имена членов передаются в виде строк в **Item**, они должны быть указаны в порядке возрастания числовых идентификаторов осей.</span><span class="sxs-lookup"><span data-stu-id="5f402-127">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers.</span></span> <span data-ttu-id="5f402-128">В пределах оси элементы должны быть перечислены в порядке возрастания вложенности измерений, то есть первым элементом измерения является первый элемент, а затем элементы внутренних измерений.</span><span class="sxs-lookup"><span data-stu-id="5f402-128">Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions.</span></span> <span data-ttu-id="5f402-129">Каждое измерение должно быть представлено отдельной строкой, а список строк членов должен разделяться запятыми.</span><span class="sxs-lookup"><span data-stu-id="5f402-129">Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="5f402-130">Получение ячеек по имени участника может не поддерживаться поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="5f402-130">Retrieving cells by member name may not be supported by your data provider.</span></span> <span data-ttu-id="5f402-131">Для получения дополнительных сведений обратитесь к документации по вашему поставщику.</span><span class="sxs-lookup"><span data-stu-id="5f402-131">See the documentation for your provider for more information.</span></span>


