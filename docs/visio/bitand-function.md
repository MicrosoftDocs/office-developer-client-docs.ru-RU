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
description: Возвращает 16-разрядное двоичное число, для каждого бита которого задано значение 1, только если соответствующий бит в binarynumber1 и binarynumber2 равен 1. В противном случае для бита задается значение 0.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409729"
---
# <a name="bitand-function"></a><span data-ttu-id="0584f-104">Функция BITAND</span><span class="sxs-lookup"><span data-stu-id="0584f-104">BITAND Function</span></span>

<span data-ttu-id="0584f-105">Возвращает 16-разрядное двоичное число, для каждого бита которого задано значение 1, только если соответствующий бит в binarynumber1 и binarynumber2 равен 1.</span><span class="sxs-lookup"><span data-stu-id="0584f-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="0584f-106">В противном случае для бита задается значение 0.</span><span class="sxs-lookup"><span data-stu-id="0584f-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0584f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0584f-107">Syntax</span></span>

<span data-ttu-id="0584f-108">БИТ. И (\* \* *binarynumber1* \* \*, \* \* *binarynumber2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0584f-108">BITAND(\*\* *binarynumber1* \*\*, \*\* *binarynumber2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0584f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0584f-109">Parameters</span></span>

|<span data-ttu-id="0584f-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0584f-110">**Name**</span></span>|<span data-ttu-id="0584f-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0584f-111">**Required/Optional**</span></span>|<span data-ttu-id="0584f-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0584f-112">**Data Type**</span></span>|<span data-ttu-id="0584f-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0584f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0584f-114">_Двоичные Число1_</span><span class="sxs-lookup"><span data-stu-id="0584f-114">_binary number1_</span></span> <br/> |<span data-ttu-id="0584f-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0584f-115">Required</span></span>  <br/> |<span data-ttu-id="0584f-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="0584f-116">**Numeric**</span></span> <br/> |<span data-ttu-id="0584f-117">Первое 16 – разрядное двоичное число.</span><span class="sxs-lookup"><span data-stu-id="0584f-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="0584f-118">_двоичные файлы число2_</span><span class="sxs-lookup"><span data-stu-id="0584f-118">_binary number2_</span></span> <br/> |<span data-ttu-id="0584f-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0584f-119">Required</span></span>  <br/> |<span data-ttu-id="0584f-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="0584f-120">**Numeric**</span></span> <br/> |<span data-ttu-id="0584f-121">Второй 16 – разрядный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="0584f-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0584f-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="0584f-122">Remarks</span></span>

<span data-ttu-id="0584f-123">Эту функцию можно использовать для проверки и изменения свойств фигуры, которые хранятся в виде битовых масок, например текстового формата фигуры.</span><span class="sxs-lookup"><span data-stu-id="0584f-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="0584f-124">Пример</span><span class="sxs-lookup"><span data-stu-id="0584f-124">Example</span></span>

<span data-ttu-id="0584f-125">БИТ. И (12, 6)</span><span class="sxs-lookup"><span data-stu-id="0584f-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="0584f-126">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="0584f-126">Returns 4.</span></span> <span data-ttu-id="0584f-127">Значение 12 = 0... 01100.</span><span class="sxs-lookup"><span data-stu-id="0584f-127">The 12 = 0...01100.</span></span> <span data-ttu-id="0584f-128">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="0584f-128">The 6 = 0...00110.</span></span> <span data-ttu-id="0584f-129">Таким образом, бит. И (12, 6) = 0... 00100.</span><span class="sxs-lookup"><span data-stu-id="0584f-129">Therefore, BITAND(12,6) = 0...00100.</span></span>
  

