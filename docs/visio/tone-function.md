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
# <a name="tone-function"></a><span data-ttu-id="e5feb-103">Функция TONE</span><span class="sxs-lookup"><span data-stu-id="e5feb-103">TONE Function</span></span>

<span data-ttu-id="e5feb-104">Изменяет цвет, уменьшая его насыщенность на количество, указанное в _параметре int._</span><span class="sxs-lookup"><span data-stu-id="e5feb-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e5feb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5feb-105">Syntax</span></span>

<span data-ttu-id="e5feb-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e5feb-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5feb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5feb-107">Parameters</span></span>

|<span data-ttu-id="e5feb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e5feb-108">**Name**</span></span>|<span data-ttu-id="e5feb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e5feb-109">**Required/Optional**</span></span>|<span data-ttu-id="e5feb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e5feb-110">**Data Type**</span></span>|<span data-ttu-id="e5feb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5feb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5feb-112">_color_</span><span class="sxs-lookup"><span data-stu-id="e5feb-112">_color_</span></span> <br/> |<span data-ttu-id="e5feb-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e5feb-113">Required</span></span>  <br/> |<span data-ttu-id="e5feb-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e5feb-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e5feb-115">Индекс цвета Microsoft Visio или RGB-значение цвета.</span><span class="sxs-lookup"><span data-stu-id="e5feb-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="e5feb-116">_int_</span><span class="sxs-lookup"><span data-stu-id="e5feb-116">_int_</span></span> <br/> |<span data-ttu-id="e5feb-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e5feb-117">Required</span></span>  <br/> |<span data-ttu-id="e5feb-118">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="e5feb-118">**Integer**</span></span> <br/> |<span data-ttu-id="e5feb-119">Количество, с помощью которого уменьшается насыщенность цвета.</span><span class="sxs-lookup"><span data-stu-id="e5feb-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="e5feb-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="e5feb-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e5feb-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5feb-121">Return value</span></span>

 <span data-ttu-id="e5feb-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="e5feb-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5feb-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5feb-123">Remarks</span></span>

<span data-ttu-id="e5feb-124">Верхние и нижние границы насыщенности — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="e5feb-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="e5feb-125">Для параметра int не существует ограничений по размеру, который можно передать для параметра  _int,_ но насыщенность никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="e5feb-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

