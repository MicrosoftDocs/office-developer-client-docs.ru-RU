---
title: Функция UNICHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Возвращает символ Юникода из числа.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417583"
---
# <a name="unichar-function"></a><span data-ttu-id="e3836-103">Функция UNICHAR</span><span class="sxs-lookup"><span data-stu-id="e3836-103">UNICHAR Function</span></span>

<span data-ttu-id="e3836-104">Возвращает символ Юникода из числа.</span><span class="sxs-lookup"><span data-stu-id="e3836-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e3836-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3836-105">Syntax</span></span>

<span data-ttu-id="e3836-106">UNICHAR (\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e3836-106">UNICHAR (\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e3836-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3836-107">Parameters</span></span>

|<span data-ttu-id="e3836-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e3836-108">**Name**</span></span>|<span data-ttu-id="e3836-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e3836-109">**Required/Optional**</span></span>|<span data-ttu-id="e3836-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e3836-110">**Data Type**</span></span>|<span data-ttu-id="e3836-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3836-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e3836-112">_число_</span><span class="sxs-lookup"><span data-stu-id="e3836-112">_number_</span></span> <br/> |<span data-ttu-id="e3836-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e3836-113">Required</span></span>  <br/> |<span data-ttu-id="e3836-114">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="e3836-114">**Integer**</span></span> <br/> |<span data-ttu-id="e3836-115">В качестве возвращаемой функцией функции может быть несколько часов от 1 до 65 535 (включительно).</span><span class="sxs-lookup"><span data-stu-id="e3836-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3836-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3836-116">Remarks</span></span>

<span data-ttu-id="e3836-117">Итоговая строка имеет один символ Юникода (два символа) в длину.</span><span class="sxs-lookup"><span data-stu-id="e3836-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e3836-118">Пример</span><span class="sxs-lookup"><span data-stu-id="e3836-118">Example</span></span>

<span data-ttu-id="e3836-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="e3836-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="e3836-120">Возвращает A (латинская буква A)</span><span class="sxs-lookup"><span data-stu-id="e3836-120">Returns A (Latin Capital Letter A)</span></span> 
  

