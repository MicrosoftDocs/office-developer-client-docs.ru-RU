---
title: Функция MIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251463
localization_priority: Normal
ms.assetid: b945b7c2-153f-2fc3-b768-1e975254ddf5
description: Возвращает наименьшее число из списка. Наименьший означает, что он ближе всего к отрицательному сходства.
ms.openlocfilehash: 7c9eb1a8d4ce30e7ab9253c2864ecd38474e8ff6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420838"
---
# <a name="min-function"></a><span data-ttu-id="e57d6-104">Функция MIN</span><span class="sxs-lookup"><span data-stu-id="e57d6-104">MIN Function</span></span>

<span data-ttu-id="e57d6-105">Возвращает наименьшее число из списка.</span><span class="sxs-lookup"><span data-stu-id="e57d6-105">Returns the smallest number from a list.</span></span> <span data-ttu-id="e57d6-106">Наименьший означает, что он ближе всего к отрицательному сходства.</span><span class="sxs-lookup"><span data-stu-id="e57d6-106">Smallest means closest to negative infinity.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e57d6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e57d6-107">Syntax</span></span>

<span data-ttu-id="e57d6-108">MIN(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e57d6-108">MIN(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e57d6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e57d6-109">Parameters</span></span>

|<span data-ttu-id="e57d6-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e57d6-110">**Name**</span></span>|<span data-ttu-id="e57d6-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e57d6-111">**Required/Optional**</span></span>|<span data-ttu-id="e57d6-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e57d6-112">**Data Type**</span></span>|<span data-ttu-id="e57d6-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e57d6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e57d6-114">_число1_</span><span class="sxs-lookup"><span data-stu-id="e57d6-114">_number1_</span></span> <br/> |<span data-ttu-id="e57d6-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e57d6-115">Required</span></span>  <br/> |<span data-ttu-id="e57d6-116">**Разные**</span><span class="sxs-lookup"><span data-stu-id="e57d6-116">**Varies**</span></span> <br/> |<span data-ttu-id="e57d6-117">Первый номер в списке.</span><span class="sxs-lookup"><span data-stu-id="e57d6-117">The first number in the list.</span></span>  <br/> |
| <span data-ttu-id="e57d6-118">_число2_</span><span class="sxs-lookup"><span data-stu-id="e57d6-118">_number2_</span></span> <br/> |<span data-ttu-id="e57d6-119">Необязательна</span><span class="sxs-lookup"><span data-stu-id="e57d6-119">Optional</span></span>  <br/> |<span data-ttu-id="e57d6-120">**Разные**</span><span class="sxs-lookup"><span data-stu-id="e57d6-120">**Varies**</span></span> <br/> | <span data-ttu-id="e57d6-121">Второй номер в списке.</span><span class="sxs-lookup"><span data-stu-id="e57d6-121">The second number in the list.</span></span>  <br/> |
| <span data-ttu-id="e57d6-122">_numberN_</span><span class="sxs-lookup"><span data-stu-id="e57d6-122">_numberN_</span></span> <br/> |<span data-ttu-id="e57d6-123">Необязательна</span><span class="sxs-lookup"><span data-stu-id="e57d6-123">Optional</span></span>  <br/> |<span data-ttu-id="e57d6-124">**Разные**</span><span class="sxs-lookup"><span data-stu-id="e57d6-124">**Varies**</span></span> <br/> |<span data-ttu-id="e57d6-125">N-й номер в списке.</span><span class="sxs-lookup"><span data-stu-id="e57d6-125">The nth number in the list.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e57d6-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e57d6-126">Return value</span></span>

<span data-ttu-id="e57d6-127">Разные</span><span class="sxs-lookup"><span data-stu-id="e57d6-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="e57d6-128">Пример</span><span class="sxs-lookup"><span data-stu-id="e57d6-128">Example</span></span>

<span data-ttu-id="e57d6-129">MIN(13 in,1 ft, 20 cm)</span><span class="sxs-lookup"><span data-stu-id="e57d6-129">MIN(13 in,1 ft, 20 cm)</span></span> 
  
<span data-ttu-id="e57d6-130">Возвращает 20 см.</span><span class="sxs-lookup"><span data-stu-id="e57d6-130">Returns 20 centimeters.</span></span> 
  

