---
title: Функция TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Изменяет цвет, увеличивая его яркость на величину (положительный или отрицательный), указанную в параметре int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406579"
---
# <a name="tint-function"></a><span data-ttu-id="9f605-103">Функция TINT</span><span class="sxs-lookup"><span data-stu-id="9f605-103">TINT Function</span></span>

<span data-ttu-id="9f605-104">Изменяет цвет, увеличивая его яркость на величину (положительный или отрицательный), указанную в параметре _int_ .</span><span class="sxs-lookup"><span data-stu-id="9f605-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f605-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f605-105">Syntax</span></span>

<span data-ttu-id="9f605-106">ОтТЕНОК (\* \* *Цвет* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9f605-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f605-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f605-107">Parameters</span></span>

|<span data-ttu-id="9f605-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9f605-108">**Name**</span></span>|<span data-ttu-id="9f605-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="9f605-109">**Required/Optional**</span></span>|<span data-ttu-id="9f605-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9f605-110">**Data Type**</span></span>|<span data-ttu-id="9f605-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f605-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f605-112">_color_</span><span class="sxs-lookup"><span data-stu-id="9f605-112">_color_</span></span> <br/> |<span data-ttu-id="9f605-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9f605-113">Required</span></span>  <br/> |<span data-ttu-id="9f605-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="9f605-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9f605-115">Цветовой индекс Microsoft Visio или значение RGB цвета.</span><span class="sxs-lookup"><span data-stu-id="9f605-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="9f605-116">_int_</span><span class="sxs-lookup"><span data-stu-id="9f605-116">_int_</span></span> <br/> |<span data-ttu-id="9f605-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9f605-117">Required</span></span>  <br/> |<span data-ttu-id="9f605-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="9f605-118">**Integer**</span></span> <br/> |<span data-ttu-id="9f605-119">Величина, на которую увеличивается яркость цвета.</span><span class="sxs-lookup"><span data-stu-id="9f605-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="9f605-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="9f605-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9f605-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f605-121">Return value</span></span>

 <span data-ttu-id="9f605-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="9f605-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f605-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="9f605-123">Remarks</span></span>

<span data-ttu-id="9f605-124">Верхние и нижние пределы яркости — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="9f605-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="9f605-125">Не существует ограничения на размер целого числа, которое можно передать для параметра _int_ , но яркость не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="9f605-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

