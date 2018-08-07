---
title: МЕЖДУ (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Указывает диапазон, для тестирования.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806957"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="228bf-103">МЕЖДУ (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="228bf-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="228bf-104">Указывает диапазон, для тестирования.</span><span class="sxs-lookup"><span data-stu-id="228bf-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="228bf-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="228bf-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="228bf-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="228bf-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="228bf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="228bf-107">Syntax</span></span>

 <span data-ttu-id="228bf-108">*test_expression*  [НЕ] **BETWEEN** *begin_expression* **AND** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="228bf-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="228bf-109">Оператор **между** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="228bf-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="228bf-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="228bf-110">**Argument**</span></span>|<span data-ttu-id="228bf-111">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="228bf-111">**Required**</span></span>|<span data-ttu-id="228bf-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="228bf-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="228bf-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="228bf-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="228bf-114">Да</span><span class="sxs-lookup"><span data-stu-id="228bf-114">Yes</span></span>  <br/> |<span data-ttu-id="228bf-115">Выражение для проверки в диапазоне, определенные в *begin_expression* и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="228bf-116">Должен быть один и тот же тип данных, как *begin_expression* и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="228bf-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="228bf-117">*NOT*</span></span>  <br/> |<span data-ttu-id="228bf-118">Нет</span><span class="sxs-lookup"><span data-stu-id="228bf-118">No</span></span>  <br/> |<span data-ttu-id="228bf-119">Указывает, что результат предиката должен быть инвертирован.</span><span class="sxs-lookup"><span data-stu-id="228bf-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="228bf-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="228bf-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="228bf-121">Да</span><span class="sxs-lookup"><span data-stu-id="228bf-121">Yes</span></span>  <br/> |<span data-ttu-id="228bf-122">Допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="228bf-122">A valid expression.</span></span> <span data-ttu-id="228bf-123">Должен быть один и тот же тип данных, как *test_expression* и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="228bf-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="228bf-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="228bf-125">Да</span><span class="sxs-lookup"><span data-stu-id="228bf-125">Yes</span></span>  <br/> |<span data-ttu-id="228bf-126">Допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="228bf-126">A valid expression.</span></span> <span data-ttu-id="228bf-127">Должен быть один и тот же тип данных, как *test_expression* и *begin_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="228bf-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="228bf-128">*AND*</span></span>  <br/> |<span data-ttu-id="228bf-129">Да</span><span class="sxs-lookup"><span data-stu-id="228bf-129">Yes</span></span>  <br/> |<span data-ttu-id="228bf-130">Указывает, что *test_expression* должны находиться в диапазон, указанный в параметре *begin_expression* и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="228bf-131">Тип результата</span><span class="sxs-lookup"><span data-stu-id="228bf-131">Result Type</span></span>

 <span data-ttu-id="228bf-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="228bf-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="228bf-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="228bf-133">Remarks</span></span>

 <span data-ttu-id="228bf-134">**BETWEEN** возвращает **значение TRUE,** Если значение *test_expression* больше или равны значениям *begin_expression* и меньше или равно значению *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="228bf-135">**МЕЖДУ не** возвращает **значение TRUE** , если значение *test_expression* меньше, чем значение *begin_expression* или больше, чем значение *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="228bf-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="228bf-136">Для указания исключительных диапазона, используйте больше, чем (\>) и меньше, чем операторы (\<).</span><span class="sxs-lookup"><span data-stu-id="228bf-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

