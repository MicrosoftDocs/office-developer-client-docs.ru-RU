---
title: Объект набора ячеек (ADO MD)
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
# <a name="cellset-object-ado-md"></a><span data-ttu-id="2fb03-102">Объект набора ячеек (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2fb03-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="2fb03-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fb03-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fb03-104">Представляет результаты многомерного запроса.</span><span class="sxs-lookup"><span data-stu-id="2fb03-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="2fb03-105">Это коллекция ячеек, выбранных из кубов или других целлсетс.</span><span class="sxs-lookup"><span data-stu-id="2fb03-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fb03-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fb03-106">Remarks</span></span>

<span data-ttu-id="2fb03-107">Данные в наборе **ячеек** извлекаются с помощью прямого, подобного массиву доступа.</span><span class="sxs-lookup"><span data-stu-id="2fb03-107">Data within a **Cellset** is retrieved using direct, array-like access.</span></span> <span data-ttu-id="2fb03-108">Можно "детализировать" до определенного члена, чтобы получить данные об этом члене.</span><span class="sxs-lookup"><span data-stu-id="2fb03-108">You can "drill down" to a specific member to obtain data about that member.</span></span> <span data-ttu-id="2fb03-109">Например, следующий код возвращает подпись первого элемента в первой оси в наборе ячеек с именем CST:</span><span class="sxs-lookup"><span data-stu-id="2fb03-109">For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="2fb03-110">В наборе ячеек отсутствует понятие текущей ячейки.</span><span class="sxs-lookup"><span data-stu-id="2fb03-110">There is no notion of a current cell within a cellset.</span></span> <span data-ttu-id="2fb03-111">Вместо этого свойство [Item](item-property-ado-md-cellset.md) получает определенный объект [Cell](cell-object-ado-md.md) из коллекции Cells.</span><span class="sxs-lookup"><span data-stu-id="2fb03-111">Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset.</span></span> <span data-ttu-id="2fb03-112">Аргументы свойства **Item** определяют, какая ячейка извлекается.</span><span class="sxs-lookup"><span data-stu-id="2fb03-112">The arguments of the **Item** property determine which cell is retrieved.</span></span> <span data-ttu-id="2fb03-113">Вы можете указать уникальное порядковое значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="2fb03-113">You can specify the unique ordinal value of a cell.</span></span> <span data-ttu-id="2fb03-114">Вы также можете извлекать ячейки, используя их номера позиции на каждой оси набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="2fb03-114">You can also retrieve cells by using their position numbers along each axis of the cellset.</span></span> <span data-ttu-id="2fb03-115">Дополнительные сведения об извлечении ячеек содержатся в разделе свойство [Item](item-property-ado-md-cellset.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-115">For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="2fb03-116">С помощью коллекций, методов и свойств объекта набора **ячеек** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2fb03-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="2fb03-117">Свяжите открытое подключение с объектом **Cell** , задав его свойство [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2fb03-118">Выполнение и получение результатов многомерного запроса с помощью метода [Open](open-method-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="2fb03-119">Получение **ячейки** из **коллекции с помощью** свойства [Item](item-property-ado-md-cellset.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="2fb03-120">Возвращает объекты [осей](axis-object-ado-md.md) , которые определяют набор **ячеек** с помощью коллекции [осей](axes-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="2fb03-121">Получение сведений об измерениях, используемых для фильтрации данных в наборе **ячеек** , с помощью свойства [FilterAxis](filteraxis-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2fb03-122">Возвращает или задает запрос, используемый для определения набором **ячеек** с помощью свойства [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2fb03-123">Возвращает текущее состояние набора **ячеек** (открытие, закрытие, выполнение или подключение) со свойством [State](state-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2fb03-124">Закройте открытый набор **ячеек** с помощью метода [Close](close-method-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb03-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="2fb03-125">Получение сведений о наборе **ячеек** с помощью стандартной коллекции [свойств](properties-collection-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="2fb03-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

