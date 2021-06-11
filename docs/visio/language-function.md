---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Позволяет сравнивать операции между различными языковыми представлениями. Он лучше всего используется для преобразования языковых тегов целевой группы интернет-инженерии (BCP 47) в значения локальных id (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424756"
---
# <a name="language-function"></a><span data-ttu-id="87a76-104">LANGUAGE Function</span><span class="sxs-lookup"><span data-stu-id="87a76-104">LANGUAGE Function</span></span>

<span data-ttu-id="87a76-105">Позволяет сравнивать операции между различными языковыми представлениями.</span><span class="sxs-lookup"><span data-stu-id="87a76-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="87a76-106">Он лучше всего используется для преобразования языковых тегов целевой группы интернет-инженерии (BCP 47) в значения локальных id (LCID).</span><span class="sxs-lookup"><span data-stu-id="87a76-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="87a76-107">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="87a76-107">Version Information</span></span>

<span data-ttu-id="87a76-108">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="87a76-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="87a76-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87a76-109">Syntax</span></span>

 <span data-ttu-id="87a76-110">**LANGUAGE** _(lcid_or_bcp47)_</span><span class="sxs-lookup"><span data-stu-id="87a76-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="87a76-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="87a76-111">Parameters</span></span>

|<span data-ttu-id="87a76-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="87a76-112">**Name**</span></span>|<span data-ttu-id="87a76-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="87a76-113">**Required/Optional**</span></span>|<span data-ttu-id="87a76-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="87a76-114">**Data Type**</span></span>|<span data-ttu-id="87a76-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="87a76-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="87a76-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="87a76-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="87a76-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="87a76-117">Required</span></span>  <br/> |<span data-ttu-id="87a76-118">**String**</span><span class="sxs-lookup"><span data-stu-id="87a76-118">**String**</span></span> <br/> |<span data-ttu-id="87a76-119">Значение LCID или BCP 47 для языка.</span><span class="sxs-lookup"><span data-stu-id="87a76-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="87a76-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87a76-120">Return value</span></span>

<span data-ttu-id="87a76-121">Целое число</span><span class="sxs-lookup"><span data-stu-id="87a76-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="87a76-122">Пример</span><span class="sxs-lookup"><span data-stu-id="87a76-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="87a76-123">Возвращает значение '1033'.</span><span class="sxs-lookup"><span data-stu-id="87a76-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="87a76-124">Возвращает значение "3082".</span><span class="sxs-lookup"><span data-stu-id="87a76-124">Returns a value of '3082'.</span></span>
  

