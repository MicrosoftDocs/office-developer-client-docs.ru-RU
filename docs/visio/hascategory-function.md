---
title: Функция HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Возвращает TRUE, если указанная строка находится в списке категорий фигуры.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433355"
---
# <a name="hascategory-function"></a><span data-ttu-id="1d53a-103">Функция HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="1d53a-103">HASCATEGORY Function</span></span>

<span data-ttu-id="1d53a-104">Возвращает TRUE, если указанная строка находится в списке категорий фигуры.</span><span class="sxs-lookup"><span data-stu-id="1d53a-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="1d53a-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="1d53a-105">Version Information</span></span>

<span data-ttu-id="1d53a-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="1d53a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1d53a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d53a-107">Syntax</span></span>

<span data-ttu-id="1d53a-108">HASCATEGORY (\*\* *категория* \*\* )</span><span class="sxs-lookup"><span data-stu-id="1d53a-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1d53a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d53a-109">Parameters</span></span>

|<span data-ttu-id="1d53a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1d53a-110">**Name**</span></span>|<span data-ttu-id="1d53a-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="1d53a-111">**Required/Optional**</span></span>|<span data-ttu-id="1d53a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1d53a-112">**Data Type**</span></span>|<span data-ttu-id="1d53a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d53a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1d53a-114">_категория_</span><span class="sxs-lookup"><span data-stu-id="1d53a-114">_category_</span></span> <br/> |<span data-ttu-id="1d53a-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1d53a-115">Required</span></span>  <br/> |<span data-ttu-id="1d53a-116">**String**</span><span class="sxs-lookup"><span data-stu-id="1d53a-116">**String**</span></span> <br/> |<span data-ttu-id="1d53a-117">Категория, для поиска.</span><span class="sxs-lookup"><span data-stu-id="1d53a-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1d53a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d53a-118">Return value</span></span>

 <span data-ttu-id="1d53a-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1d53a-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d53a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d53a-120">Remarks</span></span>

 <span data-ttu-id="1d53a-121">*Категории —*  это строки, определенные пользователем, которые можно использовать для классификации фигур.</span><span class="sxs-lookup"><span data-stu-id="1d53a-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="1d53a-122">Категории можно определить в ячейке User.msvShapeCategories в shapeSheet для фигуры.</span><span class="sxs-lookup"><span data-stu-id="1d53a-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="1d53a-123">Вы можете определить несколько категорий для фигуры, разделив категории с полу-двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="1d53a-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

