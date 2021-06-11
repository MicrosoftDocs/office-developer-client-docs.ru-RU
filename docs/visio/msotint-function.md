---
title: Функция MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Изменяет цвет, увеличивая его светоносность на указанный процент.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406425"
---
# <a name="msotint-function"></a><span data-ttu-id="d4c51-103">Функция MSOTINT</span><span class="sxs-lookup"><span data-stu-id="d4c51-103">MSOTINT Function</span></span>

<span data-ttu-id="d4c51-104">Изменяет цвет, увеличивая его светоносность на указанный процент.</span><span class="sxs-lookup"><span data-stu-id="d4c51-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d4c51-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="d4c51-105">Version Information</span></span>

<span data-ttu-id="d4c51-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d4c51-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d4c51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4c51-107">Syntax</span></span>

<span data-ttu-id="d4c51-108">MSOTINT(\*\* *цвет* \*\*, \*\* *deltaLum* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d4c51-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d4c51-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4c51-109">Parameters</span></span>

|<span data-ttu-id="d4c51-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d4c51-110">**Name**</span></span>|<span data-ttu-id="d4c51-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d4c51-111">**Required/Optional**</span></span>|<span data-ttu-id="d4c51-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d4c51-112">**Data Type**</span></span>|<span data-ttu-id="d4c51-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d4c51-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d4c51-114">_color_</span><span class="sxs-lookup"><span data-stu-id="d4c51-114">_color_</span></span> <br/> |<span data-ttu-id="d4c51-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d4c51-115">Required</span></span>  <br/> |<span data-ttu-id="d4c51-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="d4c51-116">**RGB**</span></span> <br/> |<span data-ttu-id="d4c51-117">Стандартное значение RGB (красный, зеленый, синий) или ссылка на цвет.</span><span class="sxs-lookup"><span data-stu-id="d4c51-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="d4c51-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="d4c51-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="d4c51-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d4c51-119">Required</span></span>  <br/> |<span data-ttu-id="d4c51-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d4c51-120">**Integer**</span></span> <br/> |<span data-ttu-id="d4c51-121">Процентное изменение в сторону белого (-100%) или черный (100%) из _значения цвета._</span><span class="sxs-lookup"><span data-stu-id="d4c51-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4c51-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4c51-122">Remarks</span></span>

<span data-ttu-id="d4c51-123">Чем _ближе_ значение цвета к белому или черному, тем меньше изменение оттенка, которое производится определенным _значением deltaLum._</span><span class="sxs-lookup"><span data-stu-id="d4c51-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

