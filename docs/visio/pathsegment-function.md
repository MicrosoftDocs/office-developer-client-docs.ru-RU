---
title: Функция PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Возвращает номер сегмента на основе 1 по указанной процентной отметке по указанному пути.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432487"
---
# <a name="pathsegment-function"></a><span data-ttu-id="10012-103">Функция PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="10012-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="10012-104">Возвращает номер сегмента на основе 1 по указанной процентной отметке по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="10012-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="10012-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10012-105">Syntax</span></span>

<span data-ttu-id="10012-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span><span class="sxs-lookup"><span data-stu-id="10012-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="10012-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="10012-107">Parameters</span></span>

|<span data-ttu-id="10012-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="10012-108">**Name**</span></span>|<span data-ttu-id="10012-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="10012-109">**Required/Optional**</span></span>|<span data-ttu-id="10012-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="10012-110">**Data Type**</span></span>|<span data-ttu-id="10012-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10012-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="10012-112">_section_</span><span class="sxs-lookup"><span data-stu-id="10012-112">_section_</span></span> <br/> |<span data-ttu-id="10012-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="10012-113">Required</span></span>  <br/> |<span data-ttu-id="10012-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="10012-114">**String**</span></span> <br/> |<span data-ttu-id="10012-115">Раздел "Геометрия", который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="10012-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="10012-116">_travel_</span><span class="sxs-lookup"><span data-stu-id="10012-116">_travel_</span></span> <br/> |<span data-ttu-id="10012-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="10012-117">Required</span></span>  <br/> |<span data-ttu-id="10012-118">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="10012-118">**Double**</span></span> <br/> |<span data-ttu-id="10012-119">Процент пройденного пути от точки начала до конечной точки.</span><span class="sxs-lookup"><span data-stu-id="10012-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="10012-120">Должно быть от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="10012-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="10012-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10012-121">Return value</span></span>

<span data-ttu-id="10012-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="10012-122">Integer</span></span>
  

