---
title: Функция SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Изменяет цвет, уменьшая его свет на количество (положительное или отрицательное), указанное в параметре int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326601"
---
# <a name="shade-function"></a><span data-ttu-id="266aa-103">Функция SHADE</span><span class="sxs-lookup"><span data-stu-id="266aa-103">SHADE Function</span></span>

<span data-ttu-id="266aa-104">Изменяет цвет, уменьшая его свет на количество (положительное или отрицательное), указанное в _параметре int._</span><span class="sxs-lookup"><span data-stu-id="266aa-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="266aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="266aa-105">Syntax</span></span>

<span data-ttu-id="266aa-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="266aa-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="266aa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="266aa-107">Parameters</span></span>

|<span data-ttu-id="266aa-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="266aa-108">**Name**</span></span>|<span data-ttu-id="266aa-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="266aa-109">**Required/Optional**</span></span>|<span data-ttu-id="266aa-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="266aa-110">**Data Type**</span></span>|<span data-ttu-id="266aa-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="266aa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="266aa-112">_color_</span><span class="sxs-lookup"><span data-stu-id="266aa-112">_color_</span></span> <br/> |<span data-ttu-id="266aa-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="266aa-113">Required</span></span>  <br/> |<span data-ttu-id="266aa-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="266aa-114">**Numeric**</span></span> <br/> |<span data-ttu-id="266aa-115">Индекс цвета Microsoft Visio или RGB-значение цвета.</span><span class="sxs-lookup"><span data-stu-id="266aa-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="266aa-116">_int_</span><span class="sxs-lookup"><span data-stu-id="266aa-116">_int_</span></span> <br/> |<span data-ttu-id="266aa-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="266aa-117">Required</span></span>  <br/> |<span data-ttu-id="266aa-118">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="266aa-118">**Integer**</span></span> <br/> |<span data-ttu-id="266aa-119">Количество, с помощью которого уменьшается светоугость цвета.</span><span class="sxs-lookup"><span data-stu-id="266aa-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="266aa-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="266aa-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="266aa-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="266aa-121">Return value</span></span>

 <span data-ttu-id="266aa-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="266aa-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="266aa-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="266aa-123">Remarks</span></span>

<span data-ttu-id="266aa-124">Верхние и нижние границы luminosity — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="266aa-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="266aa-125">Для параметра int не существует ограничений на размер допустимого  _integer,_ но luminosity никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="266aa-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Верхние и нижние границы luminosity](media/image199_ZA10173627.gif)
  

