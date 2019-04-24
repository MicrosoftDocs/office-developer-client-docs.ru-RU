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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344452"
---
# <a name="pathsegment-function"></a><span data-ttu-id="b1c23-103">Функция PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="b1c23-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="b1c23-104">Возвращает номер сегмента, основанный на 1, с указанным процентным знаком по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="b1c23-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b1c23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1c23-105">Syntax</span></span>

<span data-ttu-id="b1c23-106">PATHSEGMENT (\* \* *раздел* \* \*, \* \* *путешествие* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b1c23-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b1c23-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1c23-107">Parameters</span></span>

|<span data-ttu-id="b1c23-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b1c23-108">**Name**</span></span>|<span data-ttu-id="b1c23-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b1c23-109">**Required/Optional**</span></span>|<span data-ttu-id="b1c23-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b1c23-110">**Data Type**</span></span>|<span data-ttu-id="b1c23-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b1c23-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b1c23-112">_section_</span><span class="sxs-lookup"><span data-stu-id="b1c23-112">_section_</span></span> <br/> |<span data-ttu-id="b1c23-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b1c23-113">Required</span></span>  <br/> |<span data-ttu-id="b1c23-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b1c23-114">**String**</span></span> <br/> |<span data-ttu-id="b1c23-115">Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="b1c23-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="b1c23-116">_дающих_</span><span class="sxs-lookup"><span data-stu-id="b1c23-116">_travel_</span></span> <br/> |<span data-ttu-id="b1c23-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b1c23-117">Required</span></span>  <br/> |<span data-ttu-id="b1c23-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="b1c23-118">**Double**</span></span> <br/> |<span data-ttu-id="b1c23-119">Процент прохождения пути от точки начала до конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b1c23-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="b1c23-120">Значение должно находиться в пределах от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="b1c23-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b1c23-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1c23-121">Return value</span></span>

<span data-ttu-id="b1c23-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="b1c23-122">Integer</span></span>
  

