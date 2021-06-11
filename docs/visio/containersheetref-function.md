---
title: Функция CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Возвращает ссылку листа на указанный контейнер, содержащий фигуру.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437268"
---
# <a name="containersheetref-function"></a><span data-ttu-id="95409-103">Функция CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="95409-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="95409-104">Возвращает ссылку листа на указанный контейнер, содержащий фигуру.</span><span class="sxs-lookup"><span data-stu-id="95409-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="95409-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="95409-105">Version Information</span></span>

<span data-ttu-id="95409-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="95409-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="95409-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95409-107">Syntax</span></span>

<span data-ttu-id="95409-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\*\* [, category]\* \*\* )</span><span class="sxs-lookup"><span data-stu-id="95409-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95409-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="95409-109">Parameters</span></span>

|<span data-ttu-id="95409-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="95409-110">**Name**</span></span>|<span data-ttu-id="95409-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="95409-111">**Required/Optional**</span></span>|<span data-ttu-id="95409-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="95409-112">**Data Type**</span></span>|<span data-ttu-id="95409-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95409-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95409-114">_index_</span><span class="sxs-lookup"><span data-stu-id="95409-114">_index_</span></span> <br/> |<span data-ttu-id="95409-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95409-115">Required</span></span>  <br/> |<span data-ttu-id="95409-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="95409-116">**Integer**</span></span> <br/> |<span data-ttu-id="95409-117">Индекс контейнера на основе 1.</span><span class="sxs-lookup"><span data-stu-id="95409-117">The 1-based index of the container.</span></span> <span data-ttu-id="95409-118">Дополнительные сведения см. в комментарии.</span><span class="sxs-lookup"><span data-stu-id="95409-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="95409-119">_категория_</span><span class="sxs-lookup"><span data-stu-id="95409-119">_category_</span></span> <br/> |<span data-ttu-id="95409-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="95409-120">Optional</span></span>  <br/> |<span data-ttu-id="95409-121">**String**</span><span class="sxs-lookup"><span data-stu-id="95409-121">**String**</span></span> <br/> |<span data-ttu-id="95409-122">Категория контейнера.</span><span class="sxs-lookup"><span data-stu-id="95409-122">The category of the container.</span></span> <span data-ttu-id="95409-123">Дополнительные сведения см. в комментарии.</span><span class="sxs-lookup"><span data-stu-id="95409-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="95409-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95409-124">Return value</span></span>

<span data-ttu-id="95409-125">Ссылка ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="95409-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95409-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="95409-126">Remarks</span></span>

<span data-ttu-id="95409-127">Индекс контейнера рассчитывается на основе Z-порядка контейнеров спереди и сзади.</span><span class="sxs-lookup"><span data-stu-id="95409-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="95409-128">*Категории —*  это строки, определенные пользователем, которые можно использовать для классификации фигур.</span><span class="sxs-lookup"><span data-stu-id="95409-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="95409-129">Категории можно определить в ячейке User.msvShapeCategories в shapeSheet для фигуры.</span><span class="sxs-lookup"><span data-stu-id="95409-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="95409-130">Вы можете определить несколько категорий для фигуры, разделив категории с полу-двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="95409-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="95409-131">Если фигура не является членом контейнера или нет контейнера, который соответствует как указанному номеру индекса, так и категории, CONTAINERSHEETREF возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="95409-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="95409-132">Пример</span><span class="sxs-lookup"><span data-stu-id="95409-132">Example</span></span>

<span data-ttu-id="95409-133">CONTAINERSHEETREF (1)! Высота</span><span class="sxs-lookup"><span data-stu-id="95409-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="95409-134">Возвращает значение в ячейке Height контейнера, наиболее вперед на странице, к которой принадлежит фигура.</span><span class="sxs-lookup"><span data-stu-id="95409-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

