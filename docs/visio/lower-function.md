---
title: Функция LOWER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Возвращает строку, преобразованную в нижний регистр.
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421244"
---
# <a name="lower-function"></a><span data-ttu-id="9646e-103">Функция LOWER</span><span class="sxs-lookup"><span data-stu-id="9646e-103">LOWER Function</span></span>

<span data-ttu-id="9646e-104">Возвращает строку, преобразованную в нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="9646e-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9646e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9646e-105">Syntax</span></span>

<span data-ttu-id="9646e-106">LOWER (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9646e-106">LOWER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9646e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9646e-107">Parameters</span></span>

|<span data-ttu-id="9646e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9646e-108">**Name**</span></span>|<span data-ttu-id="9646e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="9646e-109">**Required/Optional**</span></span>|<span data-ttu-id="9646e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9646e-110">**Data Type**</span></span>|<span data-ttu-id="9646e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9646e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9646e-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="9646e-112">_expression_</span></span> <br/> |<span data-ttu-id="9646e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9646e-113">Required</span></span>  <br/> |<span data-ttu-id="9646e-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="9646e-114">**Varies**</span></span> <br/> | <span data-ttu-id="9646e-115">Строка, ссылка на ячейку или выражение; результат преобразуется в строку, которая затем преобразуется в нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="9646e-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9646e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9646e-116">Return value</span></span>

<span data-ttu-id="9646e-117">String</span><span class="sxs-lookup"><span data-stu-id="9646e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9646e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="9646e-118">Remarks</span></span>

<span data-ttu-id="9646e-119">Преобразование регистра зависит от параметров текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="9646e-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9646e-120">Пример</span><span class="sxs-lookup"><span data-stu-id="9646e-120">Example</span></span>

<span data-ttu-id="9646e-121">НИЖНЕе ("смешанный регистр")</span><span class="sxs-lookup"><span data-stu-id="9646e-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="9646e-122">Возвращает "Mixed Case".</span><span class="sxs-lookup"><span data-stu-id="9646e-122">Returns "mixed case".</span></span> 
  

