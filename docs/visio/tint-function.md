---
title: Функция TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Изменяет цвет, увеличение яркость на величину (положительное или отрицательное), указанный в параметре int.
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815042"
---
# <a name="tint-function"></a><span data-ttu-id="04f79-103">Функция TINT</span><span class="sxs-lookup"><span data-stu-id="04f79-103">TINT Function</span></span>

<span data-ttu-id="04f79-104">Изменяет цвет, увеличение яркость на величину (положительное или отрицательное), указанный в параметре _int_ .</span><span class="sxs-lookup"><span data-stu-id="04f79-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="04f79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04f79-105">Syntax</span></span>

<span data-ttu-id="04f79-106">TINT (** *цвет* **, ** *int* **)</span><span class="sxs-lookup"><span data-stu-id="04f79-106">TINT(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="04f79-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="04f79-107">Parameters</span></span>

|<span data-ttu-id="04f79-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="04f79-108">**Name**</span></span>|<span data-ttu-id="04f79-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="04f79-109">**Required/Optional**</span></span>|<span data-ttu-id="04f79-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="04f79-110">**Data Type**</span></span>|<span data-ttu-id="04f79-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04f79-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="04f79-112">_Цвет_</span><span class="sxs-lookup"><span data-stu-id="04f79-112">_color_</span></span> <br/> |<span data-ttu-id="04f79-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="04f79-113">Required</span></span>  <br/> |<span data-ttu-id="04f79-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="04f79-114">**Numeric**</span></span> <br/> |<span data-ttu-id="04f79-115">Microsoft Visio цветовой индекс или значение цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="04f79-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="04f79-116">_int_</span><span class="sxs-lookup"><span data-stu-id="04f79-116">_int_</span></span> <br/> |<span data-ttu-id="04f79-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="04f79-117">Required</span></span>  <br/> |<span data-ttu-id="04f79-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="04f79-118">**Integer**</span></span> <br/> |<span data-ttu-id="04f79-119">Сумма, на который увеличивается яркость цвета.</span><span class="sxs-lookup"><span data-stu-id="04f79-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="04f79-120">Может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="04f79-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="04f79-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="04f79-121">Return value</span></span>

 <span data-ttu-id="04f79-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="04f79-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04f79-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="04f79-123">Remarks</span></span>

<span data-ttu-id="04f79-124">Верхние и нижние границ «яркость» — 0 и 240 соответственно.</span><span class="sxs-lookup"><span data-stu-id="04f79-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="04f79-125">Ограничения на размер целое число, которое можно передать для параметра _int_ , не существует, но яркость никогда не превышает эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="04f79-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

