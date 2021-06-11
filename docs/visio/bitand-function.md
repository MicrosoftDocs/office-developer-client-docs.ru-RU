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
description: Возвращает 16-битный двоичный номер, в котором каждый бит устанавливается до 1 только в том случае, если соответствующий бит в двоичном номере1 и binarynumber2 составляет 1. В противном случае для бита установлено 0.
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293494"
---
# <a name="bitand-function"></a><span data-ttu-id="e5ceb-104">Функция BITAND</span><span class="sxs-lookup"><span data-stu-id="e5ceb-104">BITAND Function</span></span>

<span data-ttu-id="e5ceb-105">Возвращает 16-битный двоичный номер, в котором каждый бит устанавливается до 1 только в том случае, если соответствующий бит в двоичном номере1 и binarynumber2 составляет 1.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="e5ceb-106">В противном случае для бита установлено 0.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e5ceb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5ceb-107">Syntax</span></span>

<span data-ttu-id="e5ceb-108">BITAND ***(binarynumber1***, ***binarynumber2*** )</span><span class="sxs-lookup"><span data-stu-id="e5ceb-108">BITAND(***binarynumber1***, ***binarynumber2*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5ceb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5ceb-109">Parameters</span></span>

|<span data-ttu-id="e5ceb-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e5ceb-110">**Name**</span></span>|<span data-ttu-id="e5ceb-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e5ceb-111">**Required/Optional**</span></span>|<span data-ttu-id="e5ceb-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e5ceb-112">**Data Type**</span></span>|<span data-ttu-id="e5ceb-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5ceb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5ceb-114">_двоичный номер1_</span><span class="sxs-lookup"><span data-stu-id="e5ceb-114">_binary number1_</span></span> <br/> |<span data-ttu-id="e5ceb-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5ceb-115">Required</span></span>  <br/> |<span data-ttu-id="e5ceb-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e5ceb-116">**Numeric**</span></span> <br/> |<span data-ttu-id="e5ceb-117">Первый 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="e5ceb-118">_двоичный номер2_</span><span class="sxs-lookup"><span data-stu-id="e5ceb-118">_binary number2_</span></span> <br/> |<span data-ttu-id="e5ceb-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5ceb-119">Required</span></span>  <br/> |<span data-ttu-id="e5ceb-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e5ceb-120">**Numeric**</span></span> <br/> |<span data-ttu-id="e5ceb-121">Второй 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5ceb-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5ceb-122">Remarks</span></span>

<span data-ttu-id="e5ceb-123">Эту функцию можно использовать для проверки и изменения свойств фигуры, хранимой в виде битмаксов, например текстового формата фигуры.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="e5ceb-124">Пример</span><span class="sxs-lookup"><span data-stu-id="e5ceb-124">Example</span></span>

<span data-ttu-id="e5ceb-125">BITAND (12,6)</span><span class="sxs-lookup"><span data-stu-id="e5ceb-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="e5ceb-126">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-126">Returns 4.</span></span> <span data-ttu-id="e5ceb-127">12 = 0...01100.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-127">The 12 = 0...01100.</span></span> <span data-ttu-id="e5ceb-128">6 = 0...00110.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-128">The 6 = 0...00110.</span></span> <span data-ttu-id="e5ceb-129">Таким образом, BITAND (12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-129">Therefore, BITAND(12,6) = 0...00100.</span></span>
  

