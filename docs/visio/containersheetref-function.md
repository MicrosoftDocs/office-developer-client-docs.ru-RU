---
title: Функция CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Возвращает ссылку на лист в указанный контейнер, который содержит фигуру.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813488"
---
# <a name="containersheetref-function"></a><span data-ttu-id="96662-103">Функция CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="96662-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="96662-104">Возвращает ссылку на лист в указанный контейнер, который содержит фигуру.</span><span class="sxs-lookup"><span data-stu-id="96662-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="96662-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="96662-105">Version Information</span></span>

<span data-ttu-id="96662-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="96662-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="96662-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96662-107">Syntax</span></span>

<span data-ttu-id="96662-108">CONTAINERSHEETREF (** *индекса* ** ** *[, категории]* **)</span><span class="sxs-lookup"><span data-stu-id="96662-108">CONTAINERSHEETREF(** *index* ** ** *[, category]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="96662-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="96662-109">Parameters</span></span>

|<span data-ttu-id="96662-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="96662-110">**Name**</span></span>|<span data-ttu-id="96662-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="96662-111">**Required/Optional**</span></span>|<span data-ttu-id="96662-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="96662-112">**Data Type**</span></span>|<span data-ttu-id="96662-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96662-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="96662-114">_index_</span><span class="sxs-lookup"><span data-stu-id="96662-114">_index_</span></span> <br/> |<span data-ttu-id="96662-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96662-115">Required</span></span>  <br/> |<span data-ttu-id="96662-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="96662-116">**Integer**</span></span> <br/> |<span data-ttu-id="96662-117">Индекс контейнер, основанный на 1.</span><span class="sxs-lookup"><span data-stu-id="96662-117">The 1-based index of the container.</span></span> <span data-ttu-id="96662-118">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="96662-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="96662-119">_category_</span><span class="sxs-lookup"><span data-stu-id="96662-119">_category_</span></span> <br/> |<span data-ttu-id="96662-120">Optional</span><span class="sxs-lookup"><span data-stu-id="96662-120">Optional</span></span>  <br/> |<span data-ttu-id="96662-121">**Строка**</span><span class="sxs-lookup"><span data-stu-id="96662-121">**String**</span></span> <br/> |<span data-ttu-id="96662-122">Категория контейнера.</span><span class="sxs-lookup"><span data-stu-id="96662-122">The category of the container.</span></span> <span data-ttu-id="96662-123">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="96662-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="96662-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="96662-125">Справочник по таблице свойств фигуры</span><span class="sxs-lookup"><span data-stu-id="96662-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96662-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="96662-126">Remarks</span></span>

<span data-ttu-id="96662-127">Индекс контейнером, рассчитывается на основании в z порядке контейнеров с начала до конца.</span><span class="sxs-lookup"><span data-stu-id="96662-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="96662-128">*Категории* являются пользовательских строк, которые можно использовать для упорядочивания фигур.</span><span class="sxs-lookup"><span data-stu-id="96662-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="96662-129">Можно определить категории в ячейке User.msvShapeCategories в таблице свойств фигуры для фигуры.</span><span class="sxs-lookup"><span data-stu-id="96662-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="96662-130">Можно определить нескольких категорий для фигуры на категории, разделив их точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="96662-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="96662-131">Если фигура не является членом контейнера, или если контейнер отсутствует, соответствующий заданному индексу и категории, CONTAINERSHEETREF возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="96662-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="96662-132">Пример</span><span class="sxs-lookup"><span data-stu-id="96662-132">Example</span></span>

<span data-ttu-id="96662-133">CONTAINERSHEETREF(1)! Высота</span><span class="sxs-lookup"><span data-stu-id="96662-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="96662-134">Возвращает значение в ячейке высота контейнера, наиболее прямого на странице, к которой принадлежит фигуры.</span><span class="sxs-lookup"><span data-stu-id="96662-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

