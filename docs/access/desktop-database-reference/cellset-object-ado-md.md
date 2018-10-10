---
title: Cellset Object (ADO MD)
TOCTitle: Cellset Object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f34d467d482386886539070a9cf137dd311bce2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482971"
---
# <a name="cellset-object-ado-md"></a><span data-ttu-id="486e5-102">Cellset Object (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="486e5-102">Cellset Object (ADO MD)</span></span>

<span data-ttu-id="486e5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="486e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="486e5-104">Представляет результаты запроса многомерных.</span><span class="sxs-lookup"><span data-stu-id="486e5-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="486e5-105">Это коллекция ячеек, выбранные из кубов или других наборов ячеек.</span><span class="sxs-lookup"><span data-stu-id="486e5-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="486e5-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="486e5-106">Remarks</span></span>

<span data-ttu-id="486e5-107">Данные в рамках набора **ячеек** извлекаются с помощью прямого доступа как массив.</span><span class="sxs-lookup"><span data-stu-id="486e5-107">Data within a **Cellset** is retrieved using direct, array-like access.</span></span> <span data-ttu-id="486e5-108">Вы можете «выполнить» к определенному элементу, для получения данных о этого элемента.</span><span class="sxs-lookup"><span data-stu-id="486e5-108">You can "drill down" to a specific member to obtain data about that member.</span></span> <span data-ttu-id="486e5-109">Например следующий код возвращает заголовок первого элемента в начале на оси первого набора ячеек, с именем cst:</span><span class="sxs-lookup"><span data-stu-id="486e5-109">For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="486e5-110">Нет отсутствует понятие текущей ячейки в рамках набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="486e5-110">There is no notion of a current cell within a cellset.</span></span> <span data-ttu-id="486e5-111">Вместо этого свойство [Item](item-property-ado-md-cellset.md) получает объект определенные [ячейки](cell-object-ado-md.md) из ячеек.</span><span class="sxs-lookup"><span data-stu-id="486e5-111">Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset.</span></span> <span data-ttu-id="486e5-112">Аргументы свойство **Item** определение извлекается ячейки.</span><span class="sxs-lookup"><span data-stu-id="486e5-112">The arguments of the **Item** property determine which cell is retrieved.</span></span> <span data-ttu-id="486e5-113">Можно указать уникальный порядковый номер ячейки.</span><span class="sxs-lookup"><span data-stu-id="486e5-113">You can specify the unique ordinal value of a cell.</span></span> <span data-ttu-id="486e5-114">Вы также можете получить ячейки с помощью их положение номера каждой оси ячеек.</span><span class="sxs-lookup"><span data-stu-id="486e5-114">You can also retrieve cells by using their position numbers along each axis of the cellset.</span></span> <span data-ttu-id="486e5-115">Дополнительные сведения о получении ячеек [элемента](item-property-ado-md-cellset.md) см.</span><span class="sxs-lookup"><span data-stu-id="486e5-115">For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="486e5-116">С помощью семейства сайтов, методы и свойства объекта **ячеек** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="486e5-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="486e5-117">Свяжите открытое подключение с объектом **ячеек** , задав его свойство [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="486e5-118">Выполнение и получение результатов многомерные запроса с помощью метода [Open](open-method-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="486e5-119">Получение **ячейки** из **ячеек** с помощью свойства [элемента](item-property-ado-md-cellset.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="486e5-120">Возвращает объекты [ось](axis-object-ado-md.md) , определяющие **ячеек** с коллекцией [осей](axes-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="486e5-121">Получение сведений о измерений, используемых для фильтрации данных в наборе **ячеек** с помощью свойства [FilterAxis](filteraxis-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="486e5-122">Укажите запрос, используемый для определения **ячеек** с помощью свойства [источника](source-property-ado-md.md) или возврата.</span><span class="sxs-lookup"><span data-stu-id="486e5-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="486e5-123">Возвращает текущее состояние **ячеек** (открытым, закрытым, выполнение, или подключения) со свойством [состояния](state-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="486e5-124">Закрытие открытых **ячеек** с помощью метода [Close](close-method-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="486e5-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="486e5-125">Получение сведений от поставщика об **ячеек** в стандартный ADO [Свойства](properties-collection-ado.md) коллекции.</span><span class="sxs-lookup"><span data-stu-id="486e5-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

