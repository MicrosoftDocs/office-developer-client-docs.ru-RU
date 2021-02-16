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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423666"
---
# <a name="scontentrestriction"></a><span data-ttu-id="fc3dd-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="fc3dd-103">SContentRestriction</span></span>
 
<span data-ttu-id="fc3dd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc3dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc3dd-105">Описывает ограничение содержимого, которое используется для ограничения представления таблицы только теми строками, которые содержат столбец, содержимое которого соответствует строке поиска.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc3dd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fc3dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc3dd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc3dd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="fc3dd-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="fc3dd-108">Members</span></span>

<span data-ttu-id="fc3dd-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="fc3dd-110">Параметры, определяющие уровень точности, который должен применять ограничение содержимого при проверке совпадения.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="fc3dd-111">Нижние **16** битов члена **ulFuzzyLevel** применяются к свойствам типа PT_BINARY и PT_STRING8 и должны иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fc3dd-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="fc3dd-112">FL_FULLSTRING. Чтобы найти соответствие, строка поиска **lpProp** должна содержаться в свойстве, идентифицированного **ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="fc3dd-113">FL_PREFIX: для совпадения строка поиска **lpProp** должна отображаться в начале **свойства, заденуемого ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="fc3dd-114">Эти две строки следует сравнивать только с длиной строки поиска, задаемой **lpProp.**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="fc3dd-115">FL_SUBSTRING: для совпадения строка поиска **lpProp** должна содержаться в любом месте свойства, идентифицированного **ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="fc3dd-116">Верхние **16 битов** члена **ulFuzzyLevel** применяются только к свойствам типа PT_STRING8 и могут иметь следующие значения в любом сочетании:</span><span class="sxs-lookup"><span data-stu-id="fc3dd-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="fc3dd-117">FL_IGNORECASE: сравнение должно быть выполнено без рассмотрения дела.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="fc3dd-118">FL_IGNORENONSPACE: сравнение должно игнорировать определенные в Юникоде символы, такие как диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="fc3dd-119">FL_LOOSE: сравнение должно по возможности давать вам совпадение, игнорируя символы дела и символы без интервалов.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="fc3dd-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="fc3dd-121">Тег свойства, определяющий строку свойства, проверяемую на наличие строки поиска.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="fc3dd-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-122">**lpProp**</span></span>
  
> <span data-ttu-id="fc3dd-123">Указатель на структуру значения свойства, содержащем строку, которую необходимо использовать в качестве строки поиска.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc3dd-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="fc3dd-124">Remarks</span></span>

<span data-ttu-id="fc3dd-125">В структуре **SContentRestriction** имеется два тега свойств: один в члене **ulPropTag,** а другой в члене **ulPropTag** структуры **SPropValue,** на который указывает **lpProp.**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="fc3dd-126">В обоих тегах MAPI требует только поля типа свойства и игнорирует поле идентификатора свойства.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="fc3dd-127">Тем не менее, два типа свойств должны совпадать, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается, когда ограничение используется в вызове [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="fc3dd-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="fc3dd-128">Значения, FL_FULLSTRING, FL_PREFIX и FL_SUBSTRING взаимоисключающие.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="fc3dd-129">Можно установить только один из них, и один из них должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="fc3dd-130">Их значения являются фиксированными, и поставщик должен реализовать их точно так же, как определено.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="fc3dd-131">Поставщик должен возвращать MAPI_E_TOO_COMPLEX, если не может поддерживать эти значения.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="fc3dd-132">Значения FL_IGNORECASE, FL_IGNORENONSPACE и FL_LOOSE независимы.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="fc3dd-133">В любом месте от нуля до всех трех из них можно установить.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="fc3dd-134">Их определения предоставляются только в качестве рекомендаций, и поставщик может свободно реализовать собственное значение каждого флага.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="fc3dd-135">Поставщик не должен возвращать никаких указаний об ошибке, если у него нет реализации указанного флага.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="fc3dd-136">Результат ограничения содержимого, наложенного на свойство, не задопределяется, если свойство не существует.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="fc3dd-137">Если клиент требует четкого поведения для такого ограничения и не уверен, существует ли свойство, например, это не обязательное столбец таблицы, он должен создать ограничение **AND,** чтобы присоединиться к ограничению содержимого с ограничением на существование.</span><span class="sxs-lookup"><span data-stu-id="fc3dd-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="fc3dd-138">Используйте [структуру SExistRestriction](sexistrestriction.md) для определения ограничений на существование и [структуру SAndRestriction](sandrestriction.md) для определения **ограничения AND.**</span><span class="sxs-lookup"><span data-stu-id="fc3dd-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="fc3dd-139">Дополнительные сведения о структуре **и ограничениях SContentRestriction** в целом см. в сведениях [об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="fc3dd-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc3dd-140">См. также</span><span class="sxs-lookup"><span data-stu-id="fc3dd-140">See also</span></span>

- [<span data-ttu-id="fc3dd-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fc3dd-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="fc3dd-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fc3dd-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="fc3dd-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3dd-143">MAPI Structures</span></span>](mapi-structures.md)

