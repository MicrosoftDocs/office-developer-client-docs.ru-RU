---
title: Функция CHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Возвращает для числа символов ANSI.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813364"
---
# <a name="char-function"></a><span data-ttu-id="04fce-103">Функция CHAR</span><span class="sxs-lookup"><span data-stu-id="04fce-103">CHAR Function</span></span>

<span data-ttu-id="04fce-104">Возвращает для числа символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="04fce-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="04fce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04fce-105">Syntax</span></span>

<span data-ttu-id="04fce-106">ЗНАКОВ (** *номер* **)</span><span class="sxs-lookup"><span data-stu-id="04fce-106">CHAR(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="04fce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="04fce-107">Parameters</span></span>

|<span data-ttu-id="04fce-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="04fce-108">**Name**</span></span>|<span data-ttu-id="04fce-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="04fce-109">**Required/Optional**</span></span>|<span data-ttu-id="04fce-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="04fce-110">**Data Type**</span></span>|<span data-ttu-id="04fce-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04fce-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="04fce-112">_number_</span><span class="sxs-lookup"><span data-stu-id="04fce-112">_number_</span></span> <br/> |<span data-ttu-id="04fce-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="04fce-113">Required</span></span>  <br/> |<span data-ttu-id="04fce-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="04fce-114">**Number**</span></span> <br/> |<span data-ttu-id="04fce-115">Номер, чтобы получить символ ANSI.</span><span class="sxs-lookup"><span data-stu-id="04fce-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04fce-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="04fce-116">Remarks</span></span>

<span data-ttu-id="04fce-117">Результирующую строку — один символ.</span><span class="sxs-lookup"><span data-stu-id="04fce-117">The resulting string is one character in length.</span></span> <span data-ttu-id="04fce-118">Параметр _номер_ должно быть целое число от 1 до 255 (включительно) или функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="04fce-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="04fce-119">Пример</span><span class="sxs-lookup"><span data-stu-id="04fce-119">Example</span></span>

<span data-ttu-id="04fce-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="04fce-120">CHAR(9)</span></span> 
  
<span data-ttu-id="04fce-121">Возвращает символ табуляции.</span><span class="sxs-lookup"><span data-stu-id="04fce-121">Returns the tab character.</span></span> 
  

