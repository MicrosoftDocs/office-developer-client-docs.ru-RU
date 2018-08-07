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
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814628"
---
# <a name="rept-function"></a><span data-ttu-id="23963-103">Функция REPT</span><span class="sxs-lookup"><span data-stu-id="23963-103">REPT Function</span></span>

<span data-ttu-id="23963-104">Повторяет текст заданное количество раз.</span><span class="sxs-lookup"><span data-stu-id="23963-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="23963-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23963-105">Syntax</span></span>

<span data-ttu-id="23963-106">Повтор (** *текст* **, ** *сколько_раз* **)</span><span class="sxs-lookup"><span data-stu-id="23963-106">REPT (** *text* **, ** *number_times* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="23963-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="23963-107">Parameters</span></span>

|<span data-ttu-id="23963-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="23963-108">**Name**</span></span>|<span data-ttu-id="23963-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="23963-109">**Required/Optional**</span></span>|<span data-ttu-id="23963-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="23963-110">**Data Type**</span></span>|<span data-ttu-id="23963-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23963-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="23963-112">_text_</span><span class="sxs-lookup"><span data-stu-id="23963-112">_text_</span></span> <br/> |<span data-ttu-id="23963-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="23963-113">Required</span></span>  <br/> |<span data-ttu-id="23963-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="23963-114">**String**</span></span> <br/> | <span data-ttu-id="23963-115">Текст, который необходимо повторить.</span><span class="sxs-lookup"><span data-stu-id="23963-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="23963-116">_Сколько_раз_</span><span class="sxs-lookup"><span data-stu-id="23963-116">_number_times_</span></span> <br/> |<span data-ttu-id="23963-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="23963-117">Required</span></span>  <br/> |<span data-ttu-id="23963-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="23963-118">**Number**</span></span> <br/> |<span data-ttu-id="23963-119">Положительное число, определяющее, сколько раз необходимо повторить текст.</span><span class="sxs-lookup"><span data-stu-id="23963-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23963-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="23963-120">Remarks</span></span>

<span data-ttu-id="23963-121">Если *сколько_раз* :</span><span class="sxs-lookup"><span data-stu-id="23963-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="23963-122">Нуль (0), то функция ПОВТОР возвращает «» (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="23963-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="23963-123">Не interger, оно сокращается.</span><span class="sxs-lookup"><span data-stu-id="23963-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="23963-124">Пример</span><span class="sxs-lookup"><span data-stu-id="23963-124">Example</span></span>

<span data-ttu-id="23963-125">Повтор (»\*«, 5)</span><span class="sxs-lookup"><span data-stu-id="23963-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="23963-126">Возвращает \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="23963-126">Returns \*\*\*\*\*.</span></span> 
  

