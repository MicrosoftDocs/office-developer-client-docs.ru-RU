---
title: Функция SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Изменяет цвет, уменьшая его светоотступность на количество (положительное или отрицательное), указанное в параметре int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326601"
---
# <a name="shade-function"></a><span data-ttu-id="2efc7-103">Функция SHADE</span><span class="sxs-lookup"><span data-stu-id="2efc7-103">SHADE Function</span></span>

<span data-ttu-id="2efc7-104">Изменяет цвет, уменьшая его светоотступность на количество (положительное или отрицательное), указанное в _параметре int._</span><span class="sxs-lookup"><span data-stu-id="2efc7-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2efc7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2efc7-105">Syntax</span></span>

<span data-ttu-id="2efc7-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2efc7-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2efc7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2efc7-107">Parameters</span></span>

|<span data-ttu-id="2efc7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2efc7-108">**Name**</span></span>|<span data-ttu-id="2efc7-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="2efc7-109">**Required/Optional**</span></span>|<span data-ttu-id="2efc7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="2efc7-110">**Data Type**</span></span>|<span data-ttu-id="2efc7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2efc7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2efc7-112">_color_</span><span class="sxs-lookup"><span data-stu-id="2efc7-112">_color_</span></span> <br/> |<span data-ttu-id="2efc7-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2efc7-113">Required</span></span>  <br/> |<span data-ttu-id="2efc7-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="2efc7-114">**Numeric**</span></span> <br/> |<span data-ttu-id="2efc7-115">Индекс Visio microsoft или RGB-значение цвета.</span><span class="sxs-lookup"><span data-stu-id="2efc7-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="2efc7-116">_int_</span><span class="sxs-lookup"><span data-stu-id="2efc7-116">_int_</span></span> <br/> |<span data-ttu-id="2efc7-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2efc7-117">Required</span></span>  <br/> |<span data-ttu-id="2efc7-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="2efc7-118">**Integer**</span></span> <br/> |<span data-ttu-id="2efc7-119">Количество, с помощью которого можно уменьшить светоосякость цвета.</span><span class="sxs-lookup"><span data-stu-id="2efc7-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="2efc7-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="2efc7-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2efc7-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2efc7-121">Return value</span></span>

 <span data-ttu-id="2efc7-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="2efc7-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2efc7-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="2efc7-123">Remarks</span></span>

<span data-ttu-id="2efc7-124">Верхние и нижние границы светопоявтости 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="2efc7-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="2efc7-125">Размер конечного параметра int не ограничивается,  но светоотступность никогда не превышает этих ограничений.</span><span class="sxs-lookup"><span data-stu-id="2efc7-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Верхние и нижние ограничения светопобности](media/image199_ZA10173627.gif)
  

