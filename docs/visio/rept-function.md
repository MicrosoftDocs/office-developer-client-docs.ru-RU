---
title: Функция REPT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Повторяет текст заданное число раз.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412081"
---
# <a name="rept-function"></a><span data-ttu-id="c4e77-103">Функция REPT</span><span class="sxs-lookup"><span data-stu-id="c4e77-103">REPT Function</span></span>

<span data-ttu-id="c4e77-104">Повторяет текст заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="c4e77-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c4e77-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4e77-105">Syntax</span></span>

<span data-ttu-id="c4e77-106">Повтор (\* \* *Text* \* \*, \* \* *нумбер_тимес* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c4e77-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4e77-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4e77-107">Parameters</span></span>

|<span data-ttu-id="c4e77-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c4e77-108">**Name**</span></span>|<span data-ttu-id="c4e77-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c4e77-109">**Required/Optional**</span></span>|<span data-ttu-id="c4e77-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c4e77-110">**Data Type**</span></span>|<span data-ttu-id="c4e77-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4e77-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4e77-112">_text_</span><span class="sxs-lookup"><span data-stu-id="c4e77-112">_text_</span></span> <br/> |<span data-ttu-id="c4e77-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4e77-113">Required</span></span>  <br/> |<span data-ttu-id="c4e77-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c4e77-114">**String**</span></span> <br/> | <span data-ttu-id="c4e77-115">Текст, который нужно повторить.</span><span class="sxs-lookup"><span data-stu-id="c4e77-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="c4e77-116">_нумбер_тимес_</span><span class="sxs-lookup"><span data-stu-id="c4e77-116">_number_times_</span></span> <br/> |<span data-ttu-id="c4e77-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4e77-117">Required</span></span>  <br/> |<span data-ttu-id="c4e77-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4e77-118">**Number**</span></span> <br/> |<span data-ttu-id="c4e77-119">Положительное число, указывающее количество повторений текста.</span><span class="sxs-lookup"><span data-stu-id="c4e77-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4e77-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4e77-120">Remarks</span></span>

<span data-ttu-id="c4e77-121">Если *нумбер_тимес* :</span><span class="sxs-lookup"><span data-stu-id="c4e77-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="c4e77-122">Ноль (0), повтор возвращает "" (пустой текст).</span><span class="sxs-lookup"><span data-stu-id="c4e77-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="c4e77-123">Не интержер, он усекается.</span><span class="sxs-lookup"><span data-stu-id="c4e77-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="c4e77-124">Пример</span><span class="sxs-lookup"><span data-stu-id="c4e77-124">Example</span></span>

<span data-ttu-id="c4e77-125">Повтор ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="c4e77-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="c4e77-126">Возвращает \* \* \*значение \*. \*</span><span class="sxs-lookup"><span data-stu-id="c4e77-126">Returns \*\*\*\*\*.</span></span> 
  

