---
title: Функция BITAND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в binarynumber1 и binarynumber2 — 1. В противном случае бит равен 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813250"
---
# <a name="bitand-function"></a><span data-ttu-id="90eb7-104">Функция BITAND</span><span class="sxs-lookup"><span data-stu-id="90eb7-104">BITAND Function</span></span>

<span data-ttu-id="90eb7-105">Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в binarynumber1 и binarynumber2 — 1.</span><span class="sxs-lookup"><span data-stu-id="90eb7-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="90eb7-106">В противном случае бит равен 0.</span><span class="sxs-lookup"><span data-stu-id="90eb7-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="90eb7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90eb7-107">Syntax</span></span>

<span data-ttu-id="90eb7-108">BITAND (** *binarynumber1* **, ** *binarynumber2* **)</span><span class="sxs-lookup"><span data-stu-id="90eb7-108">BITAND(** *binarynumber1* **, ** *binarynumber2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="90eb7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90eb7-109">Parameters</span></span>

|<span data-ttu-id="90eb7-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="90eb7-110">**Name**</span></span>|<span data-ttu-id="90eb7-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="90eb7-111">**Required/Optional**</span></span>|<span data-ttu-id="90eb7-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="90eb7-112">**Data Type**</span></span>|<span data-ttu-id="90eb7-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90eb7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="90eb7-114">_двоичные Число1_</span><span class="sxs-lookup"><span data-stu-id="90eb7-114">_binary number1_</span></span> <br/> |<span data-ttu-id="90eb7-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="90eb7-115">Required</span></span>  <br/> |<span data-ttu-id="90eb7-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="90eb7-116">**Numeric**</span></span> <br/> |<span data-ttu-id="90eb7-117">Первый номер двоичные 16-разрядной.</span><span class="sxs-lookup"><span data-stu-id="90eb7-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="90eb7-118">_двоичные число2_</span><span class="sxs-lookup"><span data-stu-id="90eb7-118">_binary number2_</span></span> <br/> |<span data-ttu-id="90eb7-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="90eb7-119">Required</span></span>  <br/> |<span data-ttu-id="90eb7-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="90eb7-120">**Numeric**</span></span> <br/> |<span data-ttu-id="90eb7-121">Второй 16-разрядное число двоичные.</span><span class="sxs-lookup"><span data-stu-id="90eb7-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90eb7-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="90eb7-122">Remarks</span></span>

<span data-ttu-id="90eb7-123">Эта функция используется для тестирования и изменения свойств фигуры, которые хранятся в виде битовой маски, например, текстовый формат фигуры.</span><span class="sxs-lookup"><span data-stu-id="90eb7-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="90eb7-124">Пример</span><span class="sxs-lookup"><span data-stu-id="90eb7-124">Example</span></span>

<span data-ttu-id="90eb7-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="90eb7-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="90eb7-126">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="90eb7-126">Returns 4.</span></span> <span data-ttu-id="90eb7-127">12 = 0... 01100.</span><span class="sxs-lookup"><span data-stu-id="90eb7-127">The 12 = 0...01100.</span></span> <span data-ttu-id="90eb7-128">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="90eb7-128">The 6 = 0...00110.</span></span> <span data-ttu-id="90eb7-129">Таким образом, BITAND(12,6) = 0... 00100.</span><span class="sxs-lookup"><span data-stu-id="90eb7-129">Therefore, BITAND(12,6) = 0...00100.</span></span>
  

