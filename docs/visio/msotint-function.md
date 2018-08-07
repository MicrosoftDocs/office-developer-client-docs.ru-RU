---
title: Функция MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Изменяет цвет, увеличивает яркость, в процентах.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814317"
---
# <a name="msotint-function"></a><span data-ttu-id="f20b7-103">Функция MSOTINT</span><span class="sxs-lookup"><span data-stu-id="f20b7-103">MSOTINT Function</span></span>

<span data-ttu-id="f20b7-104">Изменяет цвет, увеличивает яркость, в процентах.</span><span class="sxs-lookup"><span data-stu-id="f20b7-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="f20b7-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="f20b7-105">Version Information</span></span>

<span data-ttu-id="f20b7-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="f20b7-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f20b7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f20b7-107">Syntax</span></span>

<span data-ttu-id="f20b7-108">MSOTINT (** *цвет* **, ** *deltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="f20b7-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f20b7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f20b7-109">Parameters</span></span>

|<span data-ttu-id="f20b7-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f20b7-110">**Name**</span></span>|<span data-ttu-id="f20b7-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="f20b7-111">**Required/Optional**</span></span>|<span data-ttu-id="f20b7-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f20b7-112">**Data Type**</span></span>|<span data-ttu-id="f20b7-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f20b7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f20b7-114">_Цвет_</span><span class="sxs-lookup"><span data-stu-id="f20b7-114">_color_</span></span> <br/> |<span data-ttu-id="f20b7-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f20b7-115">Required</span></span>  <br/> |<span data-ttu-id="f20b7-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="f20b7-116">**RGB**</span></span> <br/> |<span data-ttu-id="f20b7-117">Стандартная значение цвета RGB (красный, зеленый, синий) или ссылку на цвет.</span><span class="sxs-lookup"><span data-stu-id="f20b7-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="f20b7-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="f20b7-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="f20b7-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f20b7-119">Required</span></span>  <br/> |<span data-ttu-id="f20b7-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="f20b7-120">**Integer**</span></span> <br/> |<span data-ttu-id="f20b7-121">Изменения в процентах к Технический (-100%) или черным (100%) из значение _цвета_ .</span><span class="sxs-lookup"><span data-stu-id="f20b7-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f20b7-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="f20b7-122">Remarks</span></span>

<span data-ttu-id="f20b7-123">Более подробно, значение _цвета_ Технический или черного, тем меньше изменения tint, формируемого с определенным _deltaLum_ значение.</span><span class="sxs-lookup"><span data-stu-id="f20b7-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

