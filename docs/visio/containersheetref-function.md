---
title: Функция CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Возвращает ссылку на лист указанного контейнера, который содержит фигуру.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437268"
---
# <a name="containersheetref-function"></a><span data-ttu-id="f3387-103">Функция CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="f3387-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="f3387-104">Возвращает ссылку на лист указанного контейнера, который содержит фигуру.</span><span class="sxs-lookup"><span data-stu-id="f3387-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="f3387-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="f3387-105">Version Information</span></span>

<span data-ttu-id="f3387-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="f3387-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f3387-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3387-107">Syntax</span></span>

<span data-ttu-id="f3387-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\*\* [, category]\* \*\* )</span><span class="sxs-lookup"><span data-stu-id="f3387-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f3387-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3387-109">Parameters</span></span>

|<span data-ttu-id="f3387-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f3387-110">**Name**</span></span>|<span data-ttu-id="f3387-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f3387-111">**Required/Optional**</span></span>|<span data-ttu-id="f3387-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f3387-112">**Data Type**</span></span>|<span data-ttu-id="f3387-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f3387-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f3387-114">_индекс_</span><span class="sxs-lookup"><span data-stu-id="f3387-114">_index_</span></span> <br/> |<span data-ttu-id="f3387-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="f3387-115">Required</span></span>  <br/> |<span data-ttu-id="f3387-116">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="f3387-116">**Integer**</span></span> <br/> |<span data-ttu-id="f3387-117">Индекс контейнера, основанный на 1.</span><span class="sxs-lookup"><span data-stu-id="f3387-117">The 1-based index of the container.</span></span> <span data-ttu-id="f3387-118">Дополнительные сведения см. в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="f3387-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="f3387-119">_category_</span><span class="sxs-lookup"><span data-stu-id="f3387-119">_category_</span></span> <br/> |<span data-ttu-id="f3387-120">Необязательна</span><span class="sxs-lookup"><span data-stu-id="f3387-120">Optional</span></span>  <br/> |<span data-ttu-id="f3387-121">**Строка**</span><span class="sxs-lookup"><span data-stu-id="f3387-121">**String**</span></span> <br/> |<span data-ttu-id="f3387-122">Категория контейнера.</span><span class="sxs-lookup"><span data-stu-id="f3387-122">The category of the container.</span></span> <span data-ttu-id="f3387-123">Дополнительные сведения см. в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="f3387-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f3387-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3387-124">Return value</span></span>

<span data-ttu-id="f3387-125">Справка по shapeSheet</span><span class="sxs-lookup"><span data-stu-id="f3387-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3387-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3387-126">Remarks</span></span>

<span data-ttu-id="f3387-127">Индекс контейнера рассчитывается на основе Z-порядка контейнеров от переднего до заднего.</span><span class="sxs-lookup"><span data-stu-id="f3387-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="f3387-128">*Категории —*  это определяемая пользователем строка, которую можно использовать для классификации фигур.</span><span class="sxs-lookup"><span data-stu-id="f3387-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="f3387-129">Категории можно определить в ячейке User.msvShapeCategories в таблице shapeSheet для фигуры.</span><span class="sxs-lookup"><span data-stu-id="f3387-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="f3387-130">Вы можете определить несколько категорий для фигуры, разделив их за двоеточием.</span><span class="sxs-lookup"><span data-stu-id="f3387-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="f3387-131">Если фигура не является членом контейнера или нет контейнера, который соответствует указанному индексу и категории, CONTAINERSHEETREF возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="f3387-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="f3387-132">Пример</span><span class="sxs-lookup"><span data-stu-id="f3387-132">Example</span></span>

<span data-ttu-id="f3387-133">CONTAINERSHEETREF(1)! Height</span><span class="sxs-lookup"><span data-stu-id="f3387-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="f3387-134">Возвращает значение в ячейке Height контейнера, которое больше всего перенадвигается на странице, к которой принадлежит фигура.</span><span class="sxs-lookup"><span data-stu-id="f3387-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

