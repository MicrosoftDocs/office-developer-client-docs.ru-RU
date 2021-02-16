---
title: Функция MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Изменяет цвет, уменьшая его luminosity на указанный процент.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414496"
---
# <a name="msoshade-function"></a><span data-ttu-id="87e86-103">Функция MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="87e86-103">MSOSHADE Function</span></span>

<span data-ttu-id="87e86-104">Изменяет цвет, уменьшая его luminosity на указанный процент.</span><span class="sxs-lookup"><span data-stu-id="87e86-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="87e86-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="87e86-105">Version Information</span></span>

<span data-ttu-id="87e86-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="87e86-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="87e86-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87e86-107">Syntax</span></span>

<span data-ttu-id="87e86-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span><span class="sxs-lookup"><span data-stu-id="87e86-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="87e86-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="87e86-109">Parameters</span></span>

|<span data-ttu-id="87e86-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="87e86-110">**Name**</span></span>|<span data-ttu-id="87e86-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="87e86-111">**Required/Optional**</span></span>|<span data-ttu-id="87e86-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="87e86-112">**Data Type**</span></span>|<span data-ttu-id="87e86-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="87e86-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="87e86-114">_color_</span><span class="sxs-lookup"><span data-stu-id="87e86-114">_color_</span></span> <br/> |<span data-ttu-id="87e86-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="87e86-115">Required</span></span>  <br/> |<span data-ttu-id="87e86-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="87e86-116">**RGB**</span></span> <br/> |<span data-ttu-id="87e86-117">Стандартное значение цвета RGB (красный, зеленый, синий) или ссылка на цвет.</span><span class="sxs-lookup"><span data-stu-id="87e86-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="87e86-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="87e86-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="87e86-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="87e86-119">Required</span></span>  <br/> |<span data-ttu-id="87e86-120">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="87e86-120">**Integer**</span></span> <br/> |<span data-ttu-id="87e86-121">Процентное соотношение меняется на белый (-100%) или черный (100%) из  _значения_ цвета.</span><span class="sxs-lookup"><span data-stu-id="87e86-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87e86-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="87e86-122">Remarks</span></span>

<span data-ttu-id="87e86-123">Чем _ближе значение_ цвета к белому или черному, тем меньше изменение оттенка, которое производится определенным _значением -deltaLum._</span><span class="sxs-lookup"><span data-stu-id="87e86-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

