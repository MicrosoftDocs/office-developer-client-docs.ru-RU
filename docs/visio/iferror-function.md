---
title: Функция IFERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: Возвращает вычисленный результат первичного выражения, если он не вычисляется как ошибка. В противном случае возвращает результат вычисления альтернативного выражения.
ms.openlocfilehash: 7b9b42b5c7e7053bae862ddadf17e65015d8ecc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431178"
---
# <a name="iferror-function"></a><span data-ttu-id="7e680-104">Функция IFERROR</span><span class="sxs-lookup"><span data-stu-id="7e680-104">IFERROR Function</span></span>

<span data-ttu-id="7e680-105">Возвращает вычисленный результат первичного выражения, если он не вычисляется как ошибка.</span><span class="sxs-lookup"><span data-stu-id="7e680-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="7e680-106">В противном случае возвращает результат вычисления альтернативного выражения.</span><span class="sxs-lookup"><span data-stu-id="7e680-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7e680-107">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="7e680-107">Version Information</span></span>

<span data-ttu-id="7e680-108">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="7e680-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7e680-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e680-109">Syntax</span></span>

<span data-ttu-id="7e680-110">IFERROR (\* \* *первичное выражение* \* \*, \* \* *альтернативное выражение* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7e680-110">IFERROR(\*\* *primary expression* \*\*, \*\* *alternate expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7e680-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e680-111">Parameters</span></span>

|<span data-ttu-id="7e680-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7e680-112">**Name**</span></span>|<span data-ttu-id="7e680-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="7e680-113">**Required/Optional**</span></span>|<span data-ttu-id="7e680-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7e680-114">**Data Type**</span></span>|<span data-ttu-id="7e680-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7e680-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7e680-116">_основное выражение_</span><span class="sxs-lookup"><span data-stu-id="7e680-116">_primary expression_</span></span> <br/> |<span data-ttu-id="7e680-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7e680-117">Required</span></span>  <br/> |<span data-ttu-id="7e680-118">**String**</span><span class="sxs-lookup"><span data-stu-id="7e680-118">**String**</span></span> <br/> |<span data-ttu-id="7e680-119">Первое вычисляемое выражение.</span><span class="sxs-lookup"><span data-stu-id="7e680-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="7e680-120">_альтернативное выражение_</span><span class="sxs-lookup"><span data-stu-id="7e680-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="7e680-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7e680-121">Required</span></span>  <br/> |<span data-ttu-id="7e680-122">**String**</span><span class="sxs-lookup"><span data-stu-id="7e680-122">**String**</span></span> <br/> |<span data-ttu-id="7e680-123">Альтернативное выражение для оценки того, является ли основное выражение ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7e680-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7e680-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e680-124">Return value</span></span>

<span data-ttu-id="7e680-125">Разные</span><span class="sxs-lookup"><span data-stu-id="7e680-125">Varies</span></span>
  

