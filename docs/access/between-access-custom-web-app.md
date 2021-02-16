---
title: BETWEEN (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Указывает диапазон для тестирования.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429301"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="98c37-103">BETWEEN (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="98c37-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="98c37-104">Указывает диапазон для тестирования.</span><span class="sxs-lookup"><span data-stu-id="98c37-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="98c37-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="98c37-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="98c37-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="98c37-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="98c37-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98c37-107">Syntax</span></span>

 <span data-ttu-id="98c37-108">*test_expression*  [ NOT ] **BETWEEN** *BEGIN_EXPRESSION* **AND** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="98c37-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="98c37-109">Оператор **Between** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="98c37-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="98c37-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="98c37-110">**Argument**</span></span>|<span data-ttu-id="98c37-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="98c37-111">**Required**</span></span>|<span data-ttu-id="98c37-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98c37-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="98c37-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="98c37-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="98c37-114">Да</span><span class="sxs-lookup"><span data-stu-id="98c37-114">Yes</span></span>  <br/> |<span data-ttu-id="98c37-115">Выражение, для проверки в диапазоне, определенном  *begin_expression*  и  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="98c37-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="98c37-116">Должен иметь тот же тип данных, что и begin_expression *и* *end_expression.*</span><span class="sxs-lookup"><span data-stu-id="98c37-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="98c37-117">Возвращает только термины, которые не включают операнд.</span><span class="sxs-lookup"><span data-stu-id="98c37-117">*NOT*</span></span>  <br/> |<span data-ttu-id="98c37-118">Нет</span><span class="sxs-lookup"><span data-stu-id="98c37-118">No</span></span>  <br/> |<span data-ttu-id="98c37-119">Указывает, что результат предиката должен быть отрицаен.</span><span class="sxs-lookup"><span data-stu-id="98c37-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="98c37-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="98c37-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="98c37-121">Да</span><span class="sxs-lookup"><span data-stu-id="98c37-121">Yes</span></span>  <br/> |<span data-ttu-id="98c37-122">Допустимые выражения.</span><span class="sxs-lookup"><span data-stu-id="98c37-122">A valid expression.</span></span> <span data-ttu-id="98c37-123">Должен иметь тот же тип данных, что и test_expression *и* *end_expression.*</span><span class="sxs-lookup"><span data-stu-id="98c37-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="98c37-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="98c37-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="98c37-125">Да</span><span class="sxs-lookup"><span data-stu-id="98c37-125">Yes</span></span>  <br/> |<span data-ttu-id="98c37-126">Допустимые выражения.</span><span class="sxs-lookup"><span data-stu-id="98c37-126">A valid expression.</span></span> <span data-ttu-id="98c37-127">Должен иметь тот же тип данных, что и test_expression *и* *begin_expression.*</span><span class="sxs-lookup"><span data-stu-id="98c37-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="98c37-128">Возвращает только элементы, которые соответствуют всем операндам *AND*.</span><span class="sxs-lookup"><span data-stu-id="98c37-128">*AND*</span></span>  <br/> |<span data-ttu-id="98c37-129">Да</span><span class="sxs-lookup"><span data-stu-id="98c37-129">Yes</span></span>  <br/> |<span data-ttu-id="98c37-130">Указывает, *test_expression* должны быть в диапазоне, задамом  begin_expression и *end_expression.*</span><span class="sxs-lookup"><span data-stu-id="98c37-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="98c37-131">Тип результата</span><span class="sxs-lookup"><span data-stu-id="98c37-131">Result Type</span></span>

 <span data-ttu-id="98c37-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="98c37-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98c37-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="98c37-133">Remarks</span></span>

 <span data-ttu-id="98c37-134">**BETWEEN** возвращает **значение TRUE,** если значение test_expression больше или равно значению  *begin_expression* и меньше или равно значению *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="98c37-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="98c37-135">**ЗНАЧЕНИЕ NOT BETWEEN** возвращает **значение TRUE,** *если* значение test_expression  меньше значения begin_expression или больше значения *end_expression.*</span><span class="sxs-lookup"><span data-stu-id="98c37-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="98c37-136">Чтобы указать монопольный диапазон, используйте операторы больше , чем ( ) и \> меньше, чем операторы ( \< ).</span><span class="sxs-lookup"><span data-stu-id="98c37-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

