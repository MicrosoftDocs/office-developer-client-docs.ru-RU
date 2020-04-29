---
title: Функция HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Возвращает значение TRUE, если указанная строка найдена в списке категорий фигуры.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433355"
---
# <a name="hascategory-function"></a><span data-ttu-id="aae6d-103">Функция HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="aae6d-103">HASCATEGORY Function</span></span>

<span data-ttu-id="aae6d-104">Возвращает значение TRUE, если указанная строка найдена в списке категорий фигуры.</span><span class="sxs-lookup"><span data-stu-id="aae6d-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="aae6d-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="aae6d-105">Version Information</span></span>

<span data-ttu-id="aae6d-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="aae6d-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aae6d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aae6d-107">Syntax</span></span>

<span data-ttu-id="aae6d-108">HASCATEGORY (\* \* *Category* \* \*)</span><span class="sxs-lookup"><span data-stu-id="aae6d-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aae6d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aae6d-109">Parameters</span></span>

|<span data-ttu-id="aae6d-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="aae6d-110">**Name**</span></span>|<span data-ttu-id="aae6d-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="aae6d-111">**Required/Optional**</span></span>|<span data-ttu-id="aae6d-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="aae6d-112">**Data Type**</span></span>|<span data-ttu-id="aae6d-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aae6d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aae6d-114">_категории_</span><span class="sxs-lookup"><span data-stu-id="aae6d-114">_category_</span></span> <br/> |<span data-ttu-id="aae6d-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="aae6d-115">Required</span></span>  <br/> |<span data-ttu-id="aae6d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="aae6d-116">**String**</span></span> <br/> |<span data-ttu-id="aae6d-117">Категория, для которой необходимо выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="aae6d-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aae6d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aae6d-118">Return value</span></span>

 <span data-ttu-id="aae6d-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="aae6d-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aae6d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="aae6d-120">Remarks</span></span>

 <span data-ttu-id="aae6d-121">*Категории* — это пользовательские строки, которые можно использовать для категоризации фигур.</span><span class="sxs-lookup"><span data-stu-id="aae6d-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="aae6d-122">Можно определить категории в ячейке User. Мсвшапекатегориес таблицы свойств фигуры для фигуры.</span><span class="sxs-lookup"><span data-stu-id="aae6d-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="aae6d-123">Можно определить несколько категорий для фигуры, разделяя категории точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="aae6d-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

