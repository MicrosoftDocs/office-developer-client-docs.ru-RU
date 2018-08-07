---
title: Функция MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Изменяет цвет, уменьшая яркость указанную часть.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814288"
---
# <a name="msoshade-function"></a><span data-ttu-id="bf132-103">Функция MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="bf132-103">MSOSHADE Function</span></span>

<span data-ttu-id="bf132-104">Изменяет цвет, уменьшая яркость указанную часть.</span><span class="sxs-lookup"><span data-stu-id="bf132-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="bf132-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="bf132-105">Version Information</span></span>

<span data-ttu-id="bf132-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="bf132-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bf132-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf132-107">Syntax</span></span>

<span data-ttu-id="bf132-108">MSOSHADE (** *цвет* **, ** *- deltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="bf132-108">MSOSHADE(** *color* **, ** *-deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bf132-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf132-109">Parameters</span></span>

|<span data-ttu-id="bf132-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bf132-110">**Name**</span></span>|<span data-ttu-id="bf132-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bf132-111">**Required/Optional**</span></span>|<span data-ttu-id="bf132-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bf132-112">**Data Type**</span></span>|<span data-ttu-id="bf132-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf132-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bf132-114">_Цвет_</span><span class="sxs-lookup"><span data-stu-id="bf132-114">_color_</span></span> <br/> |<span data-ttu-id="bf132-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf132-115">Required</span></span>  <br/> |<span data-ttu-id="bf132-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="bf132-116">**RGB**</span></span> <br/> |<span data-ttu-id="bf132-117">Стандартная значение цвета RGB (красный, зеленый, синий) или ссылку на цвет.</span><span class="sxs-lookup"><span data-stu-id="bf132-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="bf132-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="bf132-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="bf132-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf132-119">Required</span></span>  <br/> |<span data-ttu-id="bf132-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="bf132-120">**Integer**</span></span> <br/> |<span data-ttu-id="bf132-121">Изменения в процентах к Технический (-100%) или черным (100%) из значение _цвета_ .</span><span class="sxs-lookup"><span data-stu-id="bf132-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf132-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf132-122">Remarks</span></span>

<span data-ttu-id="bf132-123">Более подробно, значение _цвета_ Технический или черного, тем меньше изменения тень, формируемого с определенным _-deltaLum_ значение.</span><span class="sxs-lookup"><span data-stu-id="bf132-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

