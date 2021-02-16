---
title: Функция USERUI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Оценивает одно из двух выражений в зависимости от значения состояния.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420348"
---
# <a name="userui-function"></a><span data-ttu-id="64a1c-103">Функция USERUI</span><span class="sxs-lookup"><span data-stu-id="64a1c-103">USERUI Function</span></span>

<span data-ttu-id="64a1c-104">Оценивает одно из двух выражений в зависимости от значения _состояния._</span><span class="sxs-lookup"><span data-stu-id="64a1c-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="64a1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64a1c-105">Syntax</span></span>

<span data-ttu-id="64a1c-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="64a1c-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="64a1c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="64a1c-107">Parameters</span></span>

|<span data-ttu-id="64a1c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="64a1c-108">**Name**</span></span>|<span data-ttu-id="64a1c-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="64a1c-109">**Required/Optional**</span></span>|<span data-ttu-id="64a1c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="64a1c-110">**Data Type**</span></span>|<span data-ttu-id="64a1c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="64a1c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="64a1c-112">_state_</span><span class="sxs-lookup"><span data-stu-id="64a1c-112">_state_</span></span> <br/> |<span data-ttu-id="64a1c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="64a1c-113">Required</span></span>  <br/> |<span data-ttu-id="64a1c-114">**Логический**</span><span class="sxs-lookup"><span data-stu-id="64a1c-114">**Boolean**</span></span> <br/> |<span data-ttu-id="64a1c-115">Определяет, какое выражение следует оценить.</span><span class="sxs-lookup"><span data-stu-id="64a1c-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="64a1c-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="64a1c-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="64a1c-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="64a1c-117">Required</span></span>  <br/> |<span data-ttu-id="64a1c-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="64a1c-118">**String**</span></span> <br/> |<span data-ttu-id="64a1c-119">Выражение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64a1c-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="64a1c-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="64a1c-120">_userexpression_</span></span> <br/> |<span data-ttu-id="64a1c-121">Обязательно</span><span class="sxs-lookup"><span data-stu-id="64a1c-121">Required</span></span>  <br/> |<span data-ttu-id="64a1c-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="64a1c-122">**String**</span></span> <br/> |<span data-ttu-id="64a1c-123">Выражение, предоставленное пользователем.</span><span class="sxs-lookup"><span data-stu-id="64a1c-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64a1c-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="64a1c-124">Remarks</span></span>

<span data-ttu-id="64a1c-125">Если _состояние_ 0, функция USERUI оценивает _значение defaultexpression._</span><span class="sxs-lookup"><span data-stu-id="64a1c-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="64a1c-126">Если  _состояние_ 1, он оценивает  _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="64a1c-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="64a1c-127">Пример</span><span class="sxs-lookup"><span data-stu-id="64a1c-127">Example</span></span>

<span data-ttu-id="64a1c-128">USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75)</span><span class="sxs-lookup"><span data-stu-id="64a1c-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="64a1c-129">Оценивает выражение Width \* 075 и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="64a1c-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

