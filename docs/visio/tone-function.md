---
title: Функция TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Изменяет цвет, уменьшая насыщенность на величину, указанную в параметре int.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815052"
---
# <a name="tone-function"></a><span data-ttu-id="78a81-103">Функция TONE</span><span class="sxs-lookup"><span data-stu-id="78a81-103">TONE Function</span></span>

<span data-ttu-id="78a81-104">Изменяет цвет, уменьшая насыщенность на величину, указанную в параметре _int_ .</span><span class="sxs-lookup"><span data-stu-id="78a81-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78a81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78a81-105">Syntax</span></span>

<span data-ttu-id="78a81-106">СИГНАЛ (** *цвет* **, ** *int* **)</span><span class="sxs-lookup"><span data-stu-id="78a81-106">TONE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78a81-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="78a81-107">Parameters</span></span>

|<span data-ttu-id="78a81-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="78a81-108">**Name**</span></span>|<span data-ttu-id="78a81-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="78a81-109">**Required/Optional**</span></span>|<span data-ttu-id="78a81-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="78a81-110">**Data Type**</span></span>|<span data-ttu-id="78a81-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78a81-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78a81-112">_Цвет_</span><span class="sxs-lookup"><span data-stu-id="78a81-112">_color_</span></span> <br/> |<span data-ttu-id="78a81-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="78a81-113">Required</span></span>  <br/> |<span data-ttu-id="78a81-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="78a81-114">**Numeric**</span></span> <br/> |<span data-ttu-id="78a81-115">Microsoft Visio цветовой индекс или значение цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="78a81-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="78a81-116">_int_</span><span class="sxs-lookup"><span data-stu-id="78a81-116">_int_</span></span> <br/> |<span data-ttu-id="78a81-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="78a81-117">Required</span></span>  <br/> |<span data-ttu-id="78a81-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="78a81-118">**Integer**</span></span> <br/> |<span data-ttu-id="78a81-119">Значение, на которое уменьшение насыщенность цвета.</span><span class="sxs-lookup"><span data-stu-id="78a81-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="78a81-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="78a81-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="78a81-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

 <span data-ttu-id="78a81-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="78a81-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78a81-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="78a81-123">Remarks</span></span>

<span data-ttu-id="78a81-124">Верхний и нижний пределы насыщения — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="78a81-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="78a81-125">Ограничения на размер целое число, которое можно передать для параметра _int_ , не существует, но насыщенность никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="78a81-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

