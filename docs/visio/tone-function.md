---
title: Функция TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Изменяет цвет, уменьшая его насыщенность на величину, указанную в параметре int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434377"
---
# <a name="tone-function"></a><span data-ttu-id="1e3c4-103">Функция TONE</span><span class="sxs-lookup"><span data-stu-id="1e3c4-103">TONE Function</span></span>

<span data-ttu-id="1e3c4-104">Изменяет цвет, уменьшая его насыщенность на величину, указанную в параметре _int_ .</span><span class="sxs-lookup"><span data-stu-id="1e3c4-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1e3c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e3c4-105">Syntax</span></span>

<span data-ttu-id="1e3c4-106">ТОН (\* \* *Цвет* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1e3c4-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e3c4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e3c4-107">Parameters</span></span>

|<span data-ttu-id="1e3c4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-108">**Name**</span></span>|<span data-ttu-id="1e3c4-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-109">**Required/Optional**</span></span>|<span data-ttu-id="1e3c4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-110">**Data Type**</span></span>|<span data-ttu-id="1e3c4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e3c4-112">_color_</span><span class="sxs-lookup"><span data-stu-id="1e3c4-112">_color_</span></span> <br/> |<span data-ttu-id="1e3c4-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1e3c4-113">Required</span></span>  <br/> |<span data-ttu-id="1e3c4-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="1e3c4-115">Цветовой индекс Microsoft Visio или значение RGB цвета.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="1e3c4-116">_int_</span><span class="sxs-lookup"><span data-stu-id="1e3c4-116">_int_</span></span> <br/> |<span data-ttu-id="1e3c4-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1e3c4-117">Required</span></span>  <br/> |<span data-ttu-id="1e3c4-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-118">**Integer**</span></span> <br/> |<span data-ttu-id="1e3c4-119">Величина, на которую уменьшается насыщенность цвета.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="1e3c4-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1e3c4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e3c4-121">Return value</span></span>

 <span data-ttu-id="1e3c4-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="1e3c4-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e3c4-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e3c4-123">Remarks</span></span>

<span data-ttu-id="1e3c4-124">Верхние и нижние границы насыщенности равны 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="1e3c4-125">Не существует ограничения на размер целого числа, которое можно передать для параметра _int_ , но насыщенность никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

