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
description: Повторяет текст заданное количество раз.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412081"
---
# <a name="rept-function"></a><span data-ttu-id="c243b-103">Функция REPT</span><span class="sxs-lookup"><span data-stu-id="c243b-103">REPT Function</span></span>

<span data-ttu-id="c243b-104">Повторяет текст заданное количество раз.</span><span class="sxs-lookup"><span data-stu-id="c243b-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c243b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c243b-105">Syntax</span></span>

<span data-ttu-id="c243b-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c243b-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c243b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c243b-107">Parameters</span></span>

|<span data-ttu-id="c243b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c243b-108">**Name**</span></span>|<span data-ttu-id="c243b-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c243b-109">**Required/Optional**</span></span>|<span data-ttu-id="c243b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c243b-110">**Data Type**</span></span>|<span data-ttu-id="c243b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c243b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c243b-112">_text_</span><span class="sxs-lookup"><span data-stu-id="c243b-112">_text_</span></span> <br/> |<span data-ttu-id="c243b-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c243b-113">Required</span></span>  <br/> |<span data-ttu-id="c243b-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c243b-114">**String**</span></span> <br/> | <span data-ttu-id="c243b-115">Текст, который нужно повторить.</span><span class="sxs-lookup"><span data-stu-id="c243b-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="c243b-116">_number_times_</span><span class="sxs-lookup"><span data-stu-id="c243b-116">_number_times_</span></span> <br/> |<span data-ttu-id="c243b-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="c243b-117">Required</span></span>  <br/> |<span data-ttu-id="c243b-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="c243b-118">**Number**</span></span> <br/> |<span data-ttu-id="c243b-119">Положительное число, определяющие количество повторов текста.</span><span class="sxs-lookup"><span data-stu-id="c243b-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c243b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c243b-120">Remarks</span></span>

<span data-ttu-id="c243b-121">Если *number_times:*</span><span class="sxs-lookup"><span data-stu-id="c243b-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="c243b-122">Ноль (0), REPT возвращает "" (пустой текст).</span><span class="sxs-lookup"><span data-stu-id="c243b-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="c243b-123">Не является межуголным, оно усечено.</span><span class="sxs-lookup"><span data-stu-id="c243b-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="c243b-124">Пример</span><span class="sxs-lookup"><span data-stu-id="c243b-124">Example</span></span>

<span data-ttu-id="c243b-125">REPT (" \* ", 5)</span><span class="sxs-lookup"><span data-stu-id="c243b-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="c243b-126">Возвращает \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="c243b-126">Returns \*\*\*\*\*.</span></span> 
  

