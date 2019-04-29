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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420348"
---
# <a name="userui-function"></a><span data-ttu-id="b2b76-103">Функция USERUI</span><span class="sxs-lookup"><span data-stu-id="b2b76-103">USERUI Function</span></span>

<span data-ttu-id="b2b76-104">Вычисляет одно из двух выражений в зависимости от значения _State_.</span><span class="sxs-lookup"><span data-stu-id="b2b76-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b2b76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2b76-105">Syntax</span></span>

<span data-ttu-id="b2b76-106">USERUI (\* \* *State* \* \*, \* \* *дефаултекспрессион* \* \*, \* \* *усерекспрессион* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b2b76-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b2b76-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2b76-107">Parameters</span></span>

|<span data-ttu-id="b2b76-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b2b76-108">**Name**</span></span>|<span data-ttu-id="b2b76-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b2b76-109">**Required/Optional**</span></span>|<span data-ttu-id="b2b76-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b2b76-110">**Data Type**</span></span>|<span data-ttu-id="b2b76-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b2b76-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b2b76-112">_state_</span><span class="sxs-lookup"><span data-stu-id="b2b76-112">_state_</span></span> <br/> |<span data-ttu-id="b2b76-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b2b76-113">Required</span></span>  <br/> |<span data-ttu-id="b2b76-114">**Логический**</span><span class="sxs-lookup"><span data-stu-id="b2b76-114">**Boolean**</span></span> <br/> |<span data-ttu-id="b2b76-115">Определяет, какое выражение следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="b2b76-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="b2b76-116">_дефаултекспрессион_</span><span class="sxs-lookup"><span data-stu-id="b2b76-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="b2b76-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b2b76-117">Required</span></span>  <br/> |<span data-ttu-id="b2b76-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b2b76-118">**String**</span></span> <br/> |<span data-ttu-id="b2b76-119">Выражение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2b76-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="b2b76-120">_усерекспрессион_</span><span class="sxs-lookup"><span data-stu-id="b2b76-120">_userexpression_</span></span> <br/> |<span data-ttu-id="b2b76-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b2b76-121">Required</span></span>  <br/> |<span data-ttu-id="b2b76-122">**String**</span><span class="sxs-lookup"><span data-stu-id="b2b76-122">**String**</span></span> <br/> |<span data-ttu-id="b2b76-123">Выражение, предоставленное пользователем.</span><span class="sxs-lookup"><span data-stu-id="b2b76-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2b76-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2b76-124">Remarks</span></span>

<span data-ttu-id="b2b76-125">Если значение _State_ равно 0, функция USERUI оценивает значение _дефаултекспрессион_.</span><span class="sxs-lookup"><span data-stu-id="b2b76-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="b2b76-126">Если _состояние_ равно 1, вычисляется _усерекспрессион_.</span><span class="sxs-lookup"><span data-stu-id="b2b76-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="b2b76-127">Пример</span><span class="sxs-lookup"><span data-stu-id="b2b76-127">Example</span></span>

<span data-ttu-id="b2b76-128">USERUI (1, если (Width\>6in, 6In, Width), Width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="b2b76-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="b2b76-129">Оценивает ширину\*выражения. 075 и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="b2b76-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

