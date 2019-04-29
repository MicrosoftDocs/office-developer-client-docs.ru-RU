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
description: Возвращает символ ANSI для числа.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418192"
---
# <a name="char-function"></a><span data-ttu-id="b6241-103">Функция CHAR</span><span class="sxs-lookup"><span data-stu-id="b6241-103">CHAR Function</span></span>

<span data-ttu-id="b6241-104">Возвращает символ ANSI для числа.</span><span class="sxs-lookup"><span data-stu-id="b6241-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b6241-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6241-105">Syntax</span></span>

<span data-ttu-id="b6241-106">CHAR (\* \* *Number* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b6241-106">CHAR(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b6241-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6241-107">Parameters</span></span>

|<span data-ttu-id="b6241-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b6241-108">**Name**</span></span>|<span data-ttu-id="b6241-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b6241-109">**Required/Optional**</span></span>|<span data-ttu-id="b6241-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b6241-110">**Data Type**</span></span>|<span data-ttu-id="b6241-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6241-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b6241-112">_число_</span><span class="sxs-lookup"><span data-stu-id="b6241-112">_number_</span></span> <br/> |<span data-ttu-id="b6241-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b6241-113">Required</span></span>  <br/> |<span data-ttu-id="b6241-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="b6241-114">**Number**</span></span> <br/> |<span data-ttu-id="b6241-115">Число, символ ANSI которого вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="b6241-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6241-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6241-116">Remarks</span></span>

<span data-ttu-id="b6241-117">Результирующая строка — один символ в длину.</span><span class="sxs-lookup"><span data-stu-id="b6241-117">The resulting string is one character in length.</span></span> <span data-ttu-id="b6241-118">Параметр _Number_ должен быть целым числом в диапазоне от 1 до 255 (включительно), иначе функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b6241-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b6241-119">Пример</span><span class="sxs-lookup"><span data-stu-id="b6241-119">Example</span></span>

<span data-ttu-id="b6241-120">CHAR (9)</span><span class="sxs-lookup"><span data-stu-id="b6241-120">CHAR(9)</span></span> 
  
<span data-ttu-id="b6241-121">Возвращает знак табуляции.</span><span class="sxs-lookup"><span data-stu-id="b6241-121">Returns the tab character.</span></span> 
  

