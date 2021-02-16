---
title: Функция TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Изменяет цвет, увеличив его luminosity на количество (положительное или отрицательное), указанное в параметре int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406579"
---
# <a name="tint-function"></a><span data-ttu-id="530ff-103">Функция TINT</span><span class="sxs-lookup"><span data-stu-id="530ff-103">TINT Function</span></span>

<span data-ttu-id="530ff-104">Изменяет цвет, увеличив его luminosity на количество (положительное или отрицательное), указанное в _параметре int._</span><span class="sxs-lookup"><span data-stu-id="530ff-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="530ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="530ff-105">Syntax</span></span>

<span data-ttu-id="530ff-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="530ff-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="530ff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="530ff-107">Parameters</span></span>

|<span data-ttu-id="530ff-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="530ff-108">**Name**</span></span>|<span data-ttu-id="530ff-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="530ff-109">**Required/Optional**</span></span>|<span data-ttu-id="530ff-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="530ff-110">**Data Type**</span></span>|<span data-ttu-id="530ff-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="530ff-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="530ff-112">_color_</span><span class="sxs-lookup"><span data-stu-id="530ff-112">_color_</span></span> <br/> |<span data-ttu-id="530ff-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="530ff-113">Required</span></span>  <br/> |<span data-ttu-id="530ff-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="530ff-114">**Numeric**</span></span> <br/> |<span data-ttu-id="530ff-115">Индекс цвета Microsoft Visio или RGB-значение цвета.</span><span class="sxs-lookup"><span data-stu-id="530ff-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="530ff-116">_int_</span><span class="sxs-lookup"><span data-stu-id="530ff-116">_int_</span></span> <br/> |<span data-ttu-id="530ff-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="530ff-117">Required</span></span>  <br/> |<span data-ttu-id="530ff-118">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="530ff-118">**Integer**</span></span> <br/> |<span data-ttu-id="530ff-119">Количество, на которое увеличивается светоугость цвета.</span><span class="sxs-lookup"><span data-stu-id="530ff-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="530ff-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="530ff-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="530ff-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="530ff-121">Return value</span></span>

 <span data-ttu-id="530ff-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="530ff-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="530ff-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="530ff-123">Remarks</span></span>

<span data-ttu-id="530ff-124">Верхние и нижние границы luminosity — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="530ff-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="530ff-125">Для параметра  _int_ не существует ограничений на размер этого параметра, но luminosity никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="530ff-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

