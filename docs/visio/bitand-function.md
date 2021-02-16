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
description: Возвращает 16-битный двоичный номер, в котором каждый бит имеет 1, только если соответствующий бит в двоичном номере1 и двоичном номере2 имеет 1. В противном случае для бита устанавливается 0.
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293494"
---
# <a name="bitand-function"></a><span data-ttu-id="3e6f7-104">Функция BITAND</span><span class="sxs-lookup"><span data-stu-id="3e6f7-104">BITAND Function</span></span>

<span data-ttu-id="3e6f7-105">Возвращает 16-битный двоичный номер, в котором каждый бит имеет 1, только если соответствующий бит в двоичном номере1 и двоичном номере2 имеет 1.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="3e6f7-106">В противном случае для бита устанавливается 0.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3e6f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e6f7-107">Syntax</span></span>

<span data-ttu-id="3e6f7-108">BITAND(***binarynumber1***, ***binarynumber2*** )</span><span class="sxs-lookup"><span data-stu-id="3e6f7-108">BITAND(***binarynumber1***, ***binarynumber2*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3e6f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e6f7-109">Parameters</span></span>

|<span data-ttu-id="3e6f7-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3e6f7-110">**Name**</span></span>|<span data-ttu-id="3e6f7-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3e6f7-111">**Required/Optional**</span></span>|<span data-ttu-id="3e6f7-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3e6f7-112">**Data Type**</span></span>|<span data-ttu-id="3e6f7-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e6f7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3e6f7-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="3e6f7-114">_binary number1_</span></span> <br/> |<span data-ttu-id="3e6f7-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="3e6f7-115">Required</span></span>  <br/> |<span data-ttu-id="3e6f7-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3e6f7-116">**Numeric**</span></span> <br/> |<span data-ttu-id="3e6f7-117">Первый 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="3e6f7-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="3e6f7-118">_binary number2_</span></span> <br/> |<span data-ttu-id="3e6f7-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="3e6f7-119">Required</span></span>  <br/> |<span data-ttu-id="3e6f7-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3e6f7-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3e6f7-121">Второй 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e6f7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e6f7-122">Remarks</span></span>

<span data-ttu-id="3e6f7-123">Эту функцию можно использовать для проверки и изменения свойств фигуры, которые хранятся в виде битовых вешек, например для текстового формата фигуры.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="3e6f7-124">Пример</span><span class="sxs-lookup"><span data-stu-id="3e6f7-124">Example</span></span>

<span data-ttu-id="3e6f7-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="3e6f7-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="3e6f7-126">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-126">Returns 4.</span></span> <span data-ttu-id="3e6f7-127">12 = 0...01100.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-127">The 12 = 0...01100.</span></span> <span data-ttu-id="3e6f7-128">6 = 0...00110.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-128">The 6 = 0...00110.</span></span> <span data-ttu-id="3e6f7-129">Таким образом, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="3e6f7-129">Therefore, BITAND(12,6) = 0...00100.</span></span>
  

