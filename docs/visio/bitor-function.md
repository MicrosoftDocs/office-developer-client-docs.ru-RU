---
title: Функция BITOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Возвращает 16-разрядное двоичное число, в котором для каждого бита задано значение 1, если соответствующий бит в двоичных значениях Число1 или число2 имеет значение 1. Для бита устанавливается значение 0, только если соответствующий бит равен 0 в двоичных значениях Число1 и число2.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303376"
---
# <a name="bitor-function"></a><span data-ttu-id="3c99d-104">Функция BITOR</span><span class="sxs-lookup"><span data-stu-id="3c99d-104">BITOR Function</span></span>

<span data-ttu-id="3c99d-105">Возвращает 16-разрядное двоичное число, в котором для каждого бита задано значение 1, если соответствующий бит в двоичных значениях *Число1* или *число2* имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="3c99d-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="3c99d-106">Для бита устанавливается значение 0, только если соответствующий бит равен 0 в двоичных значениях *Число1* и *число2* .</span><span class="sxs-lookup"><span data-stu-id="3c99d-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3c99d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c99d-107">Syntax</span></span>

<span data-ttu-id="3c99d-108">БИТ (\* \* *двоичные числа Число1* \* \*, \* \* двоично- *число2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3c99d-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3c99d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c99d-109">Parameters</span></span>

|<span data-ttu-id="3c99d-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3c99d-110">**Name**</span></span>|<span data-ttu-id="3c99d-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3c99d-111">**Required/Optional**</span></span>|<span data-ttu-id="3c99d-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3c99d-112">**Data Type**</span></span>|<span data-ttu-id="3c99d-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c99d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3c99d-114">_Двоичные Число1_</span><span class="sxs-lookup"><span data-stu-id="3c99d-114">_binary number1_</span></span> <br/> |<span data-ttu-id="3c99d-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c99d-115">Required</span></span>  <br/> |<span data-ttu-id="3c99d-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3c99d-116">**Numeric**</span></span> <br/> |<span data-ttu-id="3c99d-117">Первое 16 – разрядное двоичное число.</span><span class="sxs-lookup"><span data-stu-id="3c99d-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="3c99d-118">_двоичные файлы число2_</span><span class="sxs-lookup"><span data-stu-id="3c99d-118">_binary number2_</span></span> <br/> |<span data-ttu-id="3c99d-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c99d-119">Required</span></span>  <br/> |<span data-ttu-id="3c99d-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3c99d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3c99d-121">Второй 16 – разрядный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="3c99d-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3c99d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c99d-122">Return value</span></span>

<span data-ttu-id="3c99d-123">16 – разрядный двоичный</span><span class="sxs-lookup"><span data-stu-id="3c99d-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="3c99d-124">Пример</span><span class="sxs-lookup"><span data-stu-id="3c99d-124">Example</span></span>

<span data-ttu-id="3c99d-125">БИТ (12, 6)</span><span class="sxs-lookup"><span data-stu-id="3c99d-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="3c99d-126">Возвращает 14.</span><span class="sxs-lookup"><span data-stu-id="3c99d-126">Returns 14.</span></span> <span data-ttu-id="3c99d-127">Значение 12 = 0... 01100.</span><span class="sxs-lookup"><span data-stu-id="3c99d-127">The 12 = 0...01100.</span></span> <span data-ttu-id="3c99d-128">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="3c99d-128">The 6 = 0...00110.</span></span> <span data-ttu-id="3c99d-129">Таким образом, бит (12, 6) = 0... 01110.</span><span class="sxs-lookup"><span data-stu-id="3c99d-129">Therefore, BITOR(12,6) = 0...01110.</span></span>
  

