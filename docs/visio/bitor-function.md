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
description: Возвращает 16-битный двоичный номер, в котором для каждого бита установлено 1, если соответствующий бит в двоичном номере1 или двоичном номере 2 — 1. Бит установлен до 0 только в том случае, если соответствующий бит 0 в двоичном номере1 и двоичном номере 2.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408084"
---
# <a name="bitor-function"></a><span data-ttu-id="3dcd3-104">Функция BITOR</span><span class="sxs-lookup"><span data-stu-id="3dcd3-104">BITOR Function</span></span>

<span data-ttu-id="3dcd3-105">Возвращает 16-битный двоичный номер, в котором для каждого бита установлено 1, если соответствующий бит в двоичном  *номере1*  или  *двоичном номере 2*  — 1.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="3dcd3-106">Бит установлен до 0 только в том случае, если соответствующий бит 0 в *двоичном номере1* и *двоичном номере 2.*</span><span class="sxs-lookup"><span data-stu-id="3dcd3-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3dcd3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dcd3-107">Syntax</span></span>

<span data-ttu-id="3dcd3-108">BITOR(\*\* *двоичный номер1* \*\*, \*\* *двоичный номер2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="3dcd3-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3dcd3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dcd3-109">Parameters</span></span>

|<span data-ttu-id="3dcd3-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3dcd3-110">**Name**</span></span>|<span data-ttu-id="3dcd3-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3dcd3-111">**Required/Optional**</span></span>|<span data-ttu-id="3dcd3-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3dcd3-112">**Data Type**</span></span>|<span data-ttu-id="3dcd3-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3dcd3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3dcd3-114">_двоичный номер1_</span><span class="sxs-lookup"><span data-stu-id="3dcd3-114">_binary number1_</span></span> <br/> |<span data-ttu-id="3dcd3-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3dcd3-115">Required</span></span>  <br/> |<span data-ttu-id="3dcd3-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3dcd3-116">**Numeric**</span></span> <br/> |<span data-ttu-id="3dcd3-117">Первый 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="3dcd3-118">_двоичный номер2_</span><span class="sxs-lookup"><span data-stu-id="3dcd3-118">_binary number2_</span></span> <br/> |<span data-ttu-id="3dcd3-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3dcd3-119">Required</span></span>  <br/> |<span data-ttu-id="3dcd3-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3dcd3-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3dcd3-121">Второй 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3dcd3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3dcd3-122">Return value</span></span>

<span data-ttu-id="3dcd3-123">16-битная двоичная</span><span class="sxs-lookup"><span data-stu-id="3dcd3-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="3dcd3-124">Пример</span><span class="sxs-lookup"><span data-stu-id="3dcd3-124">Example</span></span>

<span data-ttu-id="3dcd3-125">BITOR (12,6)</span><span class="sxs-lookup"><span data-stu-id="3dcd3-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="3dcd3-126">Возвращает 14.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-126">Returns 14.</span></span> <span data-ttu-id="3dcd3-127">12 = 0...01100.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-127">The 12 = 0...01100.</span></span> <span data-ttu-id="3dcd3-128">6 = 0...00110.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-128">The 6 = 0...00110.</span></span> <span data-ttu-id="3dcd3-129">Таким образом, BITOR (12,6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="3dcd3-129">Therefore, BITOR(12,6) = 0...01110.</span></span>
  

