---
title: Функция SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Изменяет цвет, уменьшая яркость на величину (положительное или отрицательное), указанный в параметре int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382983"
---
# <a name="shade-function"></a><span data-ttu-id="85cbe-103">Функция SHADE</span><span class="sxs-lookup"><span data-stu-id="85cbe-103">SHADE Function</span></span>

<span data-ttu-id="85cbe-104">Изменяет цвет, уменьшая яркость на величину (положительное или отрицательное), указанный в параметре _int_ .</span><span class="sxs-lookup"><span data-stu-id="85cbe-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="85cbe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85cbe-105">Syntax</span></span>

<span data-ttu-id="85cbe-106">ЗАЛИВКА (\*\* *цвет* \*\*, \*\* *int* \*\*)</span><span class="sxs-lookup"><span data-stu-id="85cbe-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="85cbe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="85cbe-107">Parameters</span></span>

|<span data-ttu-id="85cbe-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="85cbe-108">**Name**</span></span>|<span data-ttu-id="85cbe-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="85cbe-109">**Required/Optional**</span></span>|<span data-ttu-id="85cbe-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="85cbe-110">**Data Type**</span></span>|<span data-ttu-id="85cbe-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85cbe-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="85cbe-112">_Цвет_</span><span class="sxs-lookup"><span data-stu-id="85cbe-112">_color_</span></span> <br/> |<span data-ttu-id="85cbe-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="85cbe-113">Required</span></span>  <br/> |<span data-ttu-id="85cbe-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="85cbe-114">**Numeric**</span></span> <br/> |<span data-ttu-id="85cbe-115">Microsoft Visio цветовой индекс или значение цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="85cbe-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="85cbe-116">_int_</span><span class="sxs-lookup"><span data-stu-id="85cbe-116">_int_</span></span> <br/> |<span data-ttu-id="85cbe-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="85cbe-117">Required</span></span>  <br/> |<span data-ttu-id="85cbe-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="85cbe-118">**Integer**</span></span> <br/> |<span data-ttu-id="85cbe-119">Значение, на которое уменьшение яркости цвета.</span><span class="sxs-lookup"><span data-stu-id="85cbe-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="85cbe-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="85cbe-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="85cbe-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85cbe-121">Return value</span></span>

 <span data-ttu-id="85cbe-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="85cbe-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85cbe-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="85cbe-123">Remarks</span></span>

<span data-ttu-id="85cbe-124">Верхние и нижние границ «яркость» — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="85cbe-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="85cbe-125">Ограничения на размер целое число, которое можно передать для параметра _int_ , не существует, но яркость никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="85cbe-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Верхний и нижний пределы яркости](media/image199_ZA10173627.gif)
  

