---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b08d3af8c61d8ced31e822bb787d49ad90b4df54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571677"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="35bf5-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="35bf5-103">FPropContainsProp</span></span>

<span data-ttu-id="35bf5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35bf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35bf5-105">Сравнивает два значения свойств, обычно строк или двоичные массивы, если один содержит другое.</span><span class="sxs-lookup"><span data-stu-id="35bf5-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35bf5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="35bf5-106">Header file:</span></span>  <br/> |<span data-ttu-id="35bf5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="35bf5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="35bf5-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="35bf5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35bf5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35bf5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35bf5-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="35bf5-110">Called by:</span></span>  <br/> |<span data-ttu-id="35bf5-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="35bf5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="35bf5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="35bf5-112">Parameters</span></span>

<span data-ttu-id="35bf5-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="35bf5-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="35bf5-114">[in] Указатель на структуру [SPropValue](spropvalue.md) , определяющее значение свойства, которое может содержать строку поиска, на который указывает параметр _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="35bf5-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="35bf5-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="35bf5-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="35bf5-116">[in] Указатель на структуру **SPropValue** определение строку поиска, поиск **FPropContainsProp** в значение свойства, на который указывает параметр _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="35bf5-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="35bf5-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="35bf5-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="35bf5-118">[in] Параметр параметры определение уровня привыкли использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="35bf5-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="35bf5-119">**Снижение 16-разрядный** относятся к свойств типа PT_BINARY и PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="35bf5-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="35bf5-120">Они должны иметь значение только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="35bf5-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="35bf5-121">FL_FULLSTRING: Строка поиска _lpSPropValueSrc_ должно быть равно значению свойства, определяемую средством _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="35bf5-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="35bf5-122">FL_PREFIX: Строка поиска _lpSPropValueSrc_ , которые должны встречаться в начале значение свойства, определяемую средством _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="35bf5-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="35bf5-123">Только полностью заполняя длину строки поиска, указанный в параметре _lpSPropValueSrc_сравнения двух значений.</span><span class="sxs-lookup"><span data-stu-id="35bf5-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="35bf5-124">FL_SUBSTRING: Строка поиска _lpSPropValueSrc_ должны быть включены в любом месте в значение свойства, определяемую средством _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="35bf5-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="35bf5-125">**Верхний 16-разрядный** применяются только к свойств типа PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="35bf5-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="35bf5-126">Они могут применяться следующие значения в любом сочетании:</span><span class="sxs-lookup"><span data-stu-id="35bf5-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="35bf5-127">FL_IGNORECASE: Необходимо выполнить сравнение без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="35bf5-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="35bf5-128">FL_IGNORENONSPACE: Сравнение следует игнорировать определенные Юникод непробельные символы, такие как диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="35bf5-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="35bf5-129">FL_LOOSE: Сравнение следует указать соответствие по возможности без учета регистра знаков и непробельные символы.</span><span class="sxs-lookup"><span data-stu-id="35bf5-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35bf5-130">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="35bf5-130">Return value</span></span>

<span data-ttu-id="35bf5-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="35bf5-131">TRUE</span></span> 
  
> <span data-ttu-id="35bf5-132">Параметры доступны и строка поиска _lpSPropValueSrc_ содержится указанный в значение свойства _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="35bf5-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="35bf5-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="35bf5-133">FALSE</span></span> 
  
> <span data-ttu-id="35bf5-134">Сравниваемые значения свойства не типа PT_STRING8 или PT_BINARY, значения свойств относятся к различным типам или не содержится строка поиска _lpSPropValueSrc_ , как указано в значение свойства _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="35bf5-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="35bf5-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="35bf5-135">Remarks</span></span>

<span data-ttu-id="35bf5-136">Метод сравнения зависит от типы свойств, указанных в определениях свойство [SPropValue](spropvalue.md) и нечеткое уровня совет, заданного в параметре _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="35bf5-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="35bf5-137">Функции [FPropCompareProp](fpropcompareprop.md) и **FPropContainsProp** можно использовать для подготовки ограничения для создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="35bf5-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="35bf5-138">Для типа свойства PT_BINARY верхнем 16 бит _ulFuzzyLevel_ игнорируются.</span><span class="sxs-lookup"><span data-stu-id="35bf5-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="35bf5-139">Если в параметрах _ulFuzzyLevel_ отсутствует или недопустимо, выполняется точного совпадения строки full.</span><span class="sxs-lookup"><span data-stu-id="35bf5-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="35bf5-140">Дополнительные сведения о вложенности свойство Просмотр структуры [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="35bf5-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

