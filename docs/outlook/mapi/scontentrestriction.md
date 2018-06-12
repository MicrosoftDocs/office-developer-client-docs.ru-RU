---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812217"
---
# <a name="scontentrestriction"></a><span data-ttu-id="87590-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="87590-103">SContentRestriction</span></span>
 
<span data-ttu-id="87590-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87590-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87590-105">Описывается ограничение содержимого, которое используется для ограничения представление таблицы, чтобы только строки, которые включают столбец с соответствующими строке поиска содержимого.</span><span class="sxs-lookup"><span data-stu-id="87590-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87590-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87590-106">Header file:</span></span>  <br/> |<span data-ttu-id="87590-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87590-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="87590-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="87590-108">Members</span></span>

<span data-ttu-id="87590-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="87590-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="87590-110">Определение уровня привыкли, ограничение содержимого следует применять при проверке соответствия параметров.</span><span class="sxs-lookup"><span data-stu-id="87590-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="87590-111">**Нижние 16 бит** член **ulFuzzyLevel** применять для свойств типа PT_BINARY и PT_STRING8 и должен быть установлено одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="87590-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="87590-112">FL_FULLSTRING: В соответствии с, строка поиска **lpProp** должны быть включены в свойство, определяемое **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="87590-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="87590-113">FL_PREFIX: В соответствии с, строка поиска **lpProp** , которые должны встречаться в начале свойство, определяемое **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="87590-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="87590-114">Только полностью заполняя длину строки поиска, указанный в параметре **lpProp**сравнения двух строк.</span><span class="sxs-lookup"><span data-stu-id="87590-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="87590-115">FL_SUBSTRING: В соответствии с, строка поиска **lpProp** должны быть включены в любом месте в свойство, определяемое **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="87590-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="87590-116">**Верхнем 16-разрядный** члена **ulFuzzyLevel** применяются только к свойств типа PT_STRING8 и может быть установлено в любое сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="87590-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="87590-117">FL_IGNORECASE: Необходимо выполнить сравнение без учета регистр.</span><span class="sxs-lookup"><span data-stu-id="87590-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="87590-118">FL_IGNORENONSPACE: Сравнение следует игнорировать определенные Юникод дополнительный символы, такие как диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="87590-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="87590-119">FL_LOOSE: Сравнение должен привести соответствие по возможности без учета case и дополнительный символов.</span><span class="sxs-lookup"><span data-stu-id="87590-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="87590-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="87590-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="87590-121">Свойство tag идентифицирующий свойство строки для проверки вхождения строки поиска.</span><span class="sxs-lookup"><span data-stu-id="87590-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="87590-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="87590-122">**lpProp**</span></span>
  
> <span data-ttu-id="87590-123">Указатель на структуру значение свойства, которое содержит строковое значение для использования в качестве строки поиска.</span><span class="sxs-lookup"><span data-stu-id="87590-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87590-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="87590-124">Remarks</span></span>

<span data-ttu-id="87590-125">Существует два свойства теги в структуре **SContentRestriction** : один в элемент **ulPropTag** , а другая — в член **ulPropTag** структуры **SPropValue** указывает **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="87590-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="87590-126">В обоих тегов MAPI требуется только поле типа свойства и игнорирует поле идентификатора свойства.</span><span class="sxs-lookup"><span data-stu-id="87590-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="87590-127">Тем не менее должно соответствовать типы двух свойств, либо MAPI_E_TOO_COMPLEX возвращается значение при ограничении удалось вызвать [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="87590-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="87590-128">Значения FL_FULLSTRING, FL_PREFIX и FL_SUBSTRING являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="87590-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="87590-129">Можно задать только один из них и одно из них должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="87590-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="87590-130">Предопределенная их значения и поставщик должен реализовывать их так же, как определенные.</span><span class="sxs-lookup"><span data-stu-id="87590-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="87590-131">Поставщик должен возвращать MAPI_E_TOO_COMPLEX, если он не может поддерживать эти значения.</span><span class="sxs-lookup"><span data-stu-id="87590-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="87590-132">Значения FL_IGNORECASE, FL_IGNORENONSPACE и FL_LOOSE не зависят.</span><span class="sxs-lookup"><span data-stu-id="87590-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="87590-133">В любом из нуля на все три из них можно задать.</span><span class="sxs-lookup"><span data-stu-id="87590-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="87590-134">В качестве рекомендации только приведены их определения и поставщик может реализовать свой собственный особое значение каждого флага.</span><span class="sxs-lookup"><span data-stu-id="87590-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="87590-135">Поставщик не должен возвращать указаний об ошибке, если он не имеет реализации указанного флага.</span><span class="sxs-lookup"><span data-stu-id="87590-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="87590-136">В результате контента ограничения, связанные со свойством не определен, если свойство не существует.</span><span class="sxs-lookup"><span data-stu-id="87590-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="87590-137">Когда клиент требует некорректно для подобных ограничений и не является ли свойство например существует, он не был обязательный столбец таблицы его следует создать **и** ограничения для присоединения к ограничение содержимого ограничению exist.</span><span class="sxs-lookup"><span data-stu-id="87590-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="87590-138">Используйте структуру [SExistRestriction](sexistrestriction.md) , чтобы определить ограничение exist и структуру [SAndRestriction](sandrestriction.md) для определения **и** ограничение.</span><span class="sxs-lookup"><span data-stu-id="87590-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="87590-139">Дополнительные сведения о структуре **SContentRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="87590-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87590-140">См. также</span><span class="sxs-lookup"><span data-stu-id="87590-140">See also</span></span>

- [<span data-ttu-id="87590-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="87590-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="87590-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="87590-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="87590-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="87590-143">MAPI Structures</span></span>](mapi-structures.md)

