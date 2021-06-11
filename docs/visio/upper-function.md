---
title: Функция UPPER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: Возвращает строку, преобразованную в верхний шкаф.
ms.openlocfilehash: b88958526bfb5e08839077217759f7ffb50151b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415147"
---
# <a name="upper-function"></a><span data-ttu-id="718ac-103">Функция UPPER</span><span class="sxs-lookup"><span data-stu-id="718ac-103">UPPER Function</span></span>

<span data-ttu-id="718ac-104">Возвращает строку, преобразованную в верхний шкаф.</span><span class="sxs-lookup"><span data-stu-id="718ac-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="718ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="718ac-105">Syntax</span></span>

<span data-ttu-id="718ac-106">UPPER(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="718ac-106">UPPER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="718ac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="718ac-107">Parameters</span></span>

|<span data-ttu-id="718ac-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="718ac-108">**Name**</span></span>|<span data-ttu-id="718ac-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="718ac-109">**Required/Optional**</span></span>|<span data-ttu-id="718ac-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="718ac-110">**Data Type**</span></span>|<span data-ttu-id="718ac-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="718ac-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="718ac-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="718ac-112">_expression_</span></span> <br/> |<span data-ttu-id="718ac-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="718ac-113">Required</span></span>  <br/> |<span data-ttu-id="718ac-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="718ac-114">**Varies**</span></span> <br/> | <span data-ttu-id="718ac-115">Строка, ссылка ячейки или выражение; результат преобразуется в строку, которая затем преобразуется в верхний шкаф.</span><span class="sxs-lookup"><span data-stu-id="718ac-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="718ac-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="718ac-116">Remarks</span></span>

<span data-ttu-id="718ac-117">Преобразование дела зависит от конкретного локального параметра, основанного на текущих параметрах пользователя.</span><span class="sxs-lookup"><span data-stu-id="718ac-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="718ac-118">Пример</span><span class="sxs-lookup"><span data-stu-id="718ac-118">Example</span></span>

<span data-ttu-id="718ac-119">UPPER ("mIxEd CAse")</span><span class="sxs-lookup"><span data-stu-id="718ac-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="718ac-120">Возвращает "СМЕШАННЫЙ СЛУЧАЙ".</span><span class="sxs-lookup"><span data-stu-id="718ac-120">Returns "MIXED CASE".</span></span> 
  

