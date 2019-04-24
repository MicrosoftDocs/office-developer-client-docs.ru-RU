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
description: Вычисляет одно из двух выражений в зависимости от значения State.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331327"
---
# <a name="userui-function"></a><span data-ttu-id="e5dfc-103">Функция USERUI</span><span class="sxs-lookup"><span data-stu-id="e5dfc-103">USERUI Function</span></span>

<span data-ttu-id="e5dfc-104">Вычисляет одно из двух выражений в зависимости от значения _State_.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e5dfc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5dfc-105">Syntax</span></span>

<span data-ttu-id="e5dfc-106">USERUI (\* \* *State* \* \*, \* \* *дефаултекспрессион* \* \*, \* \* *усерекспрессион* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e5dfc-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5dfc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5dfc-107">Parameters</span></span>

|<span data-ttu-id="e5dfc-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-108">**Name**</span></span>|<span data-ttu-id="e5dfc-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-109">**Required/Optional**</span></span>|<span data-ttu-id="e5dfc-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-110">**Data Type**</span></span>|<span data-ttu-id="e5dfc-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5dfc-112">_state_</span><span class="sxs-lookup"><span data-stu-id="e5dfc-112">_state_</span></span> <br/> |<span data-ttu-id="e5dfc-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5dfc-113">Required</span></span>  <br/> |<span data-ttu-id="e5dfc-114">**Логический**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-114">**Boolean**</span></span> <br/> |<span data-ttu-id="e5dfc-115">Определяет, какое выражение следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="e5dfc-116">_дефаултекспрессион_</span><span class="sxs-lookup"><span data-stu-id="e5dfc-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="e5dfc-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5dfc-117">Required</span></span>  <br/> |<span data-ttu-id="e5dfc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-118">**String**</span></span> <br/> |<span data-ttu-id="e5dfc-119">Выражение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="e5dfc-120">_усерекспрессион_</span><span class="sxs-lookup"><span data-stu-id="e5dfc-120">_userexpression_</span></span> <br/> |<span data-ttu-id="e5dfc-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5dfc-121">Required</span></span>  <br/> |<span data-ttu-id="e5dfc-122">**String**</span><span class="sxs-lookup"><span data-stu-id="e5dfc-122">**String**</span></span> <br/> |<span data-ttu-id="e5dfc-123">Выражение, предоставленное пользователем.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5dfc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5dfc-124">Remarks</span></span>

<span data-ttu-id="e5dfc-125">Если значение _State_ равно 0, функция USERUI оценивает значение _дефаултекспрессион_.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="e5dfc-126">Если _состояние_ равно 1, вычисляется _усерекспрессион_.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="e5dfc-127">Пример</span><span class="sxs-lookup"><span data-stu-id="e5dfc-127">Example</span></span>

<span data-ttu-id="e5dfc-128">USERUI (1, если (Width\>6in, 6In, Width), Width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="e5dfc-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="e5dfc-129">Оценивает ширину\*выражения. 075 и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="e5dfc-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

