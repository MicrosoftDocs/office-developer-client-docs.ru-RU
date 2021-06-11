---
title: Функция TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Изменяет цвет, уменьшая его насыщенность на количество, указанное в параметре int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434377"
---
# <a name="tone-function"></a><span data-ttu-id="54044-103">Функция TONE</span><span class="sxs-lookup"><span data-stu-id="54044-103">TONE Function</span></span>

<span data-ttu-id="54044-104">Изменяет цвет, уменьшая его насыщенность на количество, указанное в _параметре int._</span><span class="sxs-lookup"><span data-stu-id="54044-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="54044-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54044-105">Syntax</span></span>

<span data-ttu-id="54044-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="54044-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="54044-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="54044-107">Parameters</span></span>

|<span data-ttu-id="54044-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="54044-108">**Name**</span></span>|<span data-ttu-id="54044-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="54044-109">**Required/Optional**</span></span>|<span data-ttu-id="54044-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="54044-110">**Data Type**</span></span>|<span data-ttu-id="54044-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="54044-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="54044-112">_color_</span><span class="sxs-lookup"><span data-stu-id="54044-112">_color_</span></span> <br/> |<span data-ttu-id="54044-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="54044-113">Required</span></span>  <br/> |<span data-ttu-id="54044-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="54044-114">**Numeric**</span></span> <br/> |<span data-ttu-id="54044-115">Индекс Visio microsoft или RGB-значение цвета.</span><span class="sxs-lookup"><span data-stu-id="54044-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="54044-116">_int_</span><span class="sxs-lookup"><span data-stu-id="54044-116">_int_</span></span> <br/> |<span data-ttu-id="54044-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="54044-117">Required</span></span>  <br/> |<span data-ttu-id="54044-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="54044-118">**Integer**</span></span> <br/> |<span data-ttu-id="54044-119">Количество, с помощью которого можно уменьшить насыщенность цвета.</span><span class="sxs-lookup"><span data-stu-id="54044-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="54044-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="54044-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="54044-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54044-121">Return value</span></span>

 <span data-ttu-id="54044-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="54044-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54044-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="54044-123">Remarks</span></span>

<span data-ttu-id="54044-124">Верхние и нижние границы насыщенности — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="54044-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="54044-125">Размер конечного параметра int не ограничивается,  но насыщенность никогда не превышает этих ограничений.</span><span class="sxs-lookup"><span data-stu-id="54044-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

