---
title: Функция PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Возвращает номер сегмента, основанный на 1, с указанным процентным знаком по указанному пути.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432487"
---
# <a name="pathsegment-function"></a><span data-ttu-id="233f9-103">Функция PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="233f9-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="233f9-104">Возвращает номер сегмента, основанный на 1, с указанным процентным знаком по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="233f9-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="233f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="233f9-105">Syntax</span></span>

<span data-ttu-id="233f9-106">PATHSEGMENT (\* \* *раздел* \* \*, \* \* *путешествие* \* \*)</span><span class="sxs-lookup"><span data-stu-id="233f9-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="233f9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="233f9-107">Parameters</span></span>

|<span data-ttu-id="233f9-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="233f9-108">**Name**</span></span>|<span data-ttu-id="233f9-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="233f9-109">**Required/Optional**</span></span>|<span data-ttu-id="233f9-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="233f9-110">**Data Type**</span></span>|<span data-ttu-id="233f9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="233f9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="233f9-112">_section_</span><span class="sxs-lookup"><span data-stu-id="233f9-112">_section_</span></span> <br/> |<span data-ttu-id="233f9-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="233f9-113">Required</span></span>  <br/> |<span data-ttu-id="233f9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="233f9-114">**String**</span></span> <br/> |<span data-ttu-id="233f9-115">Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="233f9-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="233f9-116">_дающих_</span><span class="sxs-lookup"><span data-stu-id="233f9-116">_travel_</span></span> <br/> |<span data-ttu-id="233f9-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="233f9-117">Required</span></span>  <br/> |<span data-ttu-id="233f9-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="233f9-118">**Double**</span></span> <br/> |<span data-ttu-id="233f9-119">Процент прохождения пути от точки начала до конечной точки.</span><span class="sxs-lookup"><span data-stu-id="233f9-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="233f9-120">Значение должно находиться в пределах от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="233f9-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="233f9-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="233f9-121">Return value</span></span>

<span data-ttu-id="233f9-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="233f9-122">Integer</span></span>
  

