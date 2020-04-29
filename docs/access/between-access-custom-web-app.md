---
title: МЕЖДУ (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Указывает диапазон для проверки.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429301"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="869d3-103">МЕЖДУ (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="869d3-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="869d3-104">Указывает диапазон для проверки.</span><span class="sxs-lookup"><span data-stu-id="869d3-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="869d3-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="869d3-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="869d3-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="869d3-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="869d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="869d3-107">Syntax</span></span>

 <span data-ttu-id="869d3-108">*test_expression* [NOT] **между** *begin_expression* **и** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="869d3-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="869d3-109">Оператор **between** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="869d3-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="869d3-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="869d3-110">**Argument**</span></span>|<span data-ttu-id="869d3-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="869d3-111">**Required**</span></span>|<span data-ttu-id="869d3-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="869d3-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="869d3-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="869d3-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="869d3-114">Да</span><span class="sxs-lookup"><span data-stu-id="869d3-114">Yes</span></span>  <br/> |<span data-ttu-id="869d3-115">Выражение для проверки в диапазоне, определяемом *begin_expression* и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="869d3-116">Должны иметь тот же тип данных, что и *begin_expression* , и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="869d3-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="869d3-117">*NOT*</span></span>  <br/> |<span data-ttu-id="869d3-118">Нет</span><span class="sxs-lookup"><span data-stu-id="869d3-118">No</span></span>  <br/> |<span data-ttu-id="869d3-119">Указывает, что результат предиката должен быть инвертирован.</span><span class="sxs-lookup"><span data-stu-id="869d3-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="869d3-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="869d3-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="869d3-121">Да</span><span class="sxs-lookup"><span data-stu-id="869d3-121">Yes</span></span>  <br/> |<span data-ttu-id="869d3-122">Допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="869d3-122">A valid expression.</span></span> <span data-ttu-id="869d3-123">Должны иметь тот же тип данных, что и *test_expression* , и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="869d3-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="869d3-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="869d3-125">Да</span><span class="sxs-lookup"><span data-stu-id="869d3-125">Yes</span></span>  <br/> |<span data-ttu-id="869d3-126">Допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="869d3-126">A valid expression.</span></span> <span data-ttu-id="869d3-127">Должны иметь тот же тип данных, что и *test_expression* , и *begin_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="869d3-128">*И*</span><span class="sxs-lookup"><span data-stu-id="869d3-128">*AND*</span></span>  <br/> |<span data-ttu-id="869d3-129">Да</span><span class="sxs-lookup"><span data-stu-id="869d3-129">Yes</span></span>  <br/> |<span data-ttu-id="869d3-130">Указывает, что *test_expression* должны находиться в диапазоне, указанном *begin_expression* , и *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="869d3-131">Тип результата</span><span class="sxs-lookup"><span data-stu-id="869d3-131">Result Type</span></span>

 <span data-ttu-id="869d3-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="869d3-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="869d3-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="869d3-133">Remarks</span></span>

 <span data-ttu-id="869d3-134">**Возвращает** значение **true** , если значение *test_expression* больше или равно значению *begin_expression* и меньше или равно значению *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="869d3-135">**NOT BETWEEN** возвращает **true** , если значение *test_expression* меньше значения *begin_expression* или больше значения *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="869d3-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="869d3-136">Чтобы указать монопольный диапазон, используйте операторы больше (\>) и меньше, чем (\<).</span><span class="sxs-lookup"><span data-stu-id="869d3-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

