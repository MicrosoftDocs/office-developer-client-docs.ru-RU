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
# <a name="cellset-object-ado-md"></a><span data-ttu-id="4c067-102">Объект Cellset (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4c067-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="4c067-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c067-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c067-104">Представляет результаты многомерного запроса.</span><span class="sxs-lookup"><span data-stu-id="4c067-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="4c067-105">Это коллекция ячеек, выбранных из кубов или других ячеек.</span><span class="sxs-lookup"><span data-stu-id="4c067-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c067-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="4c067-106">Remarks</span></span>

<span data-ttu-id="4c067-107">Данные в **ячейках извлекаются** с помощью прямого доступа, подобного массиву.</span><span class="sxs-lookup"><span data-stu-id="4c067-107">Data within a **Cellset** is retrieved using direct, array-like access.</span></span> <span data-ttu-id="4c067-108">Вы можете "развернуть" определенный член, чтобы получить данные об этом члене.</span><span class="sxs-lookup"><span data-stu-id="4c067-108">You can "drill down" to a specific member to obtain data about that member.</span></span> <span data-ttu-id="4c067-109">Например, следующий код возвращает заголовок первого члена в первой позиции на первой оси ячейки cst:</span><span class="sxs-lookup"><span data-stu-id="4c067-109">For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="4c067-110">В ячейках нет представления о текущей ячейке.</span><span class="sxs-lookup"><span data-stu-id="4c067-110">There is no notion of a current cell within a cellset.</span></span> <span data-ttu-id="4c067-111">Вместо этого свойство [Item](item-property-ado-md-cellset.md) извлекает определенный объект [Cell](cell-object-ado-md.md) из ячейки.</span><span class="sxs-lookup"><span data-stu-id="4c067-111">Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset.</span></span> <span data-ttu-id="4c067-112">Аргументы свойства **Item** определяют извлекаемую ячейку.</span><span class="sxs-lookup"><span data-stu-id="4c067-112">The arguments of the **Item** property determine which cell is retrieved.</span></span> <span data-ttu-id="4c067-113">Можно указать уникальное порядковое значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="4c067-113">You can specify the unique ordinal value of a cell.</span></span> <span data-ttu-id="4c067-114">Вы также можете получить ячейки, используя их номера позиции вдоль каждой оси ячеек.</span><span class="sxs-lookup"><span data-stu-id="4c067-114">You can also retrieve cells by using their position numbers along each axis of the cellset.</span></span> <span data-ttu-id="4c067-115">Дополнительные сведения о том, как получить ячейки, см. в [свойстве Item.](item-property-ado-md-cellset.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-115">For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="4c067-116">С помощью коллекций, методов и свойств объекта **Cellset** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="4c067-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="4c067-117">Связывание открытого подключения с объектом **Cellset** путем установки его свойства [ActiveConnection.](activeconnection-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4c067-118">Выполнение и извлечение результатов многомерного запроса с помощью метода [Open.](open-method-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="4c067-119">**Извлечение ячейки** из **ячейки с** [свойством Item.](item-property-ado-md-cellset.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="4c067-120">Возвращает [объекты Axis,](axis-object-ado-md.md) которые определяют **ячейки с** [коллекцией Axes.](axes-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="4c067-121">Извлекать сведения об измерениях, используемых  для фильтрации данных в ячейках с помощью свойства [FilterAxis.](filteraxis-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4c067-122">Возвращает или указывает запрос, используемый для определения **ячейки с** помощью [свойства Source.](source-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4c067-123">Возвращает текущее состояние **cellset** (открытие, закрытое, выполнение или подключение) со [свойством State.](state-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4c067-124">Закроем **открытый ячейки** с помощью метода [Close.](close-method-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="4c067-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="4c067-125">Извлечение сведений о **cellset** для конкретного поставщика со стандартной коллекцией [свойств](properties-collection-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="4c067-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

