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
description: Возвращает строку, преобразовать в нижний регистр.
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814185"
---
# <a name="lower-function"></a><span data-ttu-id="91a3c-103">Функция LOWER</span><span class="sxs-lookup"><span data-stu-id="91a3c-103">LOWER Function</span></span>

<span data-ttu-id="91a3c-104">Возвращает строку, преобразовать в нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="91a3c-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="91a3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91a3c-105">Syntax</span></span>

<span data-ttu-id="91a3c-106">Снижение (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="91a3c-106">LOWER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="91a3c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="91a3c-107">Parameters</span></span>

|<span data-ttu-id="91a3c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="91a3c-108">**Name**</span></span>|<span data-ttu-id="91a3c-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="91a3c-109">**Required/Optional**</span></span>|<span data-ttu-id="91a3c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="91a3c-110">**Data Type**</span></span>|<span data-ttu-id="91a3c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="91a3c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="91a3c-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="91a3c-112">_expression_</span></span> <br/> |<span data-ttu-id="91a3c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="91a3c-113">Required</span></span>  <br/> |<span data-ttu-id="91a3c-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="91a3c-114">**Varies**</span></span> <br/> | <span data-ttu-id="91a3c-115">Строка, ссылка на ячейку или выражение; результат преобразуется в строку, который затем преобразуется в нижний регистр.</span><span class="sxs-lookup"><span data-stu-id="91a3c-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="91a3c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="91a3c-117">Строка</span><span class="sxs-lookup"><span data-stu-id="91a3c-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91a3c-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="91a3c-118">Remarks</span></span>

<span data-ttu-id="91a3c-119">Преобразование регистра конкретных языковых стандартов на основании текущих параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="91a3c-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="91a3c-120">Пример</span><span class="sxs-lookup"><span data-stu-id="91a3c-120">Example</span></span>

<span data-ttu-id="91a3c-121">Снижение ("смешанная CAse")</span><span class="sxs-lookup"><span data-stu-id="91a3c-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="91a3c-122">Возврат значения «смешанное case».</span><span class="sxs-lookup"><span data-stu-id="91a3c-122">Returns "mixed case".</span></span> 
  

