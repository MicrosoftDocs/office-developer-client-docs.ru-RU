---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Разрешает операции сравнения между различными представлениями языка. Его лучше всего использовать для преобразования значений тегов языка для задач проектирования через Интернет (BCP 47) в значения идентификатора языкового стандарта (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327820"
---
# <a name="language-function"></a><span data-ttu-id="afebf-104">LANGUAGE Function</span><span class="sxs-lookup"><span data-stu-id="afebf-104">LANGUAGE Function</span></span>

<span data-ttu-id="afebf-105">Разрешает операции сравнения между различными представлениями языка.</span><span class="sxs-lookup"><span data-stu-id="afebf-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="afebf-106">Его лучше всего использовать для преобразования значений тегов языка для задач проектирования через Интернет (BCP 47) в значения идентификатора языкового стандарта (LCID).</span><span class="sxs-lookup"><span data-stu-id="afebf-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="afebf-107">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="afebf-107">Version Information</span></span>

<span data-ttu-id="afebf-108">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="afebf-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="afebf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afebf-109">Syntax</span></span>

 <span data-ttu-id="afebf-110">**Language (язык** ) ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="afebf-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="afebf-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="afebf-111">Parameters</span></span>

|<span data-ttu-id="afebf-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="afebf-112">**Name**</span></span>|<span data-ttu-id="afebf-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="afebf-113">**Required/Optional**</span></span>|<span data-ttu-id="afebf-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="afebf-114">**Data Type**</span></span>|<span data-ttu-id="afebf-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="afebf-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="afebf-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="afebf-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="afebf-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="afebf-117">Required</span></span>  <br/> |<span data-ttu-id="afebf-118">**String**</span><span class="sxs-lookup"><span data-stu-id="afebf-118">**String**</span></span> <br/> |<span data-ttu-id="afebf-119">Значение LCID или BCP 47 для языка.</span><span class="sxs-lookup"><span data-stu-id="afebf-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="afebf-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afebf-120">Return value</span></span>

<span data-ttu-id="afebf-121">Целое число</span><span class="sxs-lookup"><span data-stu-id="afebf-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="afebf-122">Пример</span><span class="sxs-lookup"><span data-stu-id="afebf-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="afebf-123">Возвращает значение "1033".</span><span class="sxs-lookup"><span data-stu-id="afebf-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="afebf-124">Возвращает значение "3082".</span><span class="sxs-lookup"><span data-stu-id="afebf-124">Returns a value of '3082'.</span></span>
  

