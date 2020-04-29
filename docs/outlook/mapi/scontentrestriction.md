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
# <a name="scontentrestriction"></a><span data-ttu-id="ef93f-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="ef93f-103">SContentRestriction</span></span>
 
<span data-ttu-id="ef93f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef93f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef93f-105">Описывает ограничение содержимого, используемое для ограничения представления таблицы только теми строками, которые содержат столбец с содержимым, совпадающим со строкой поиска.</span><span class="sxs-lookup"><span data-stu-id="ef93f-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef93f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ef93f-106">Header file:</span></span>  <br/> |<span data-ttu-id="ef93f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ef93f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="ef93f-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="ef93f-108">Members</span></span>

<span data-ttu-id="ef93f-109">**улфуззилевел**</span><span class="sxs-lookup"><span data-stu-id="ef93f-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="ef93f-110">Параметр Option определяет уровень точности, который должен обеспечивать ограничение содержимого при проверке соответствия.</span><span class="sxs-lookup"><span data-stu-id="ef93f-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="ef93f-111">**Младшие 16 разрядов** элемента **улфуззилевел** применяются к свойствам типа PT_BINARY и PT_STRING8 и должны иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ef93f-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="ef93f-112">FL_FULLSTRING: для сравнения строка поиска **лппроп** должна содержаться в свойстве, определенном **улпроптаг**.</span><span class="sxs-lookup"><span data-stu-id="ef93f-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="ef93f-113">FL_PREFIX: для сравнения строка поиска **лппроп** должна находиться в начале свойства, идентифицируемого **улпроптаг**.</span><span class="sxs-lookup"><span data-stu-id="ef93f-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="ef93f-114">Две строки должны сравниваться только до длины строки поиска, указанной в **лппроп**.</span><span class="sxs-lookup"><span data-stu-id="ef93f-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="ef93f-115">FL_SUBSTRING: для сравнения строка поиска **лппроп** должна содержаться в любом месте свойства, определенного **улпроптаг**.</span><span class="sxs-lookup"><span data-stu-id="ef93f-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="ef93f-116">**Верхние 16 разрядов** элемента **улфуззилевел** применяются только к свойствам типа PT_STRING8 и могут быть заданы следующие значения в любой комбинации:</span><span class="sxs-lookup"><span data-stu-id="ef93f-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="ef93f-117">FL_IGNORECASE: сравнение следует производить без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="ef93f-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="ef93f-118">FL_IGNORENONSPACE: сравнение должно игнорировать символы, не являющиеся пробелами в Юникоде, например диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="ef93f-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="ef93f-119">FL_LOOSE: при сравнении должно быть найдено соответствие по возможности, игнорируя символы Case и не пробелы.</span><span class="sxs-lookup"><span data-stu-id="ef93f-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="ef93f-120">**улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="ef93f-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="ef93f-121">Тег Property, определяющий свойство String, которое должно быть проверено на наличие искомой строки.</span><span class="sxs-lookup"><span data-stu-id="ef93f-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="ef93f-122">**лппроп**</span><span class="sxs-lookup"><span data-stu-id="ef93f-122">**lpProp**</span></span>
  
> <span data-ttu-id="ef93f-123">Указатель на структуру значения свойства, которая содержит строковое значение, используемое в качестве строки поиска.</span><span class="sxs-lookup"><span data-stu-id="ef93f-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef93f-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef93f-124">Remarks</span></span>

<span data-ttu-id="ef93f-125">В структуре **сконтентрестриктион** есть два тега свойств: один в элементе **улпроптаг** , а другой в элементе **улпроптаг** структуры **спропвалуе** , на который указывает **лппроп**.</span><span class="sxs-lookup"><span data-stu-id="ef93f-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="ef93f-126">В обоих тегах для MAPI требуется только поле Тип свойства и значение поля идентификатора свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ef93f-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="ef93f-127">Тем не менее, эти два типа свойств должны быть согласованы, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается, если ограничение используется при вызове [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="ef93f-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="ef93f-128">Значения FL_FULLSTRING, FL_PREFIX и FL_SUBSTRING являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="ef93f-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="ef93f-129">Можно задать только одно из них, а одно из них должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="ef93f-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="ef93f-130">Их значения фиксированы, и поставщик должен реализовать их в точности так, как определено.</span><span class="sxs-lookup"><span data-stu-id="ef93f-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="ef93f-131">Поставщик должен возвратить MAPI_E_TOO_COMPLEX, если он не может поддерживать эти значения.</span><span class="sxs-lookup"><span data-stu-id="ef93f-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="ef93f-132">Значения FL_IGNORECASE, FL_IGNORENONSPACE и FL_LOOSE независимы друг от друга.</span><span class="sxs-lookup"><span data-stu-id="ef93f-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="ef93f-133">Можно задать любое значение от нуля до всех трех.</span><span class="sxs-lookup"><span data-stu-id="ef93f-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="ef93f-134">Их определения предоставляются только в качестве рекомендации, и поставщик может реализовать собственное конкретное значение каждого флага.</span><span class="sxs-lookup"><span data-stu-id="ef93f-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="ef93f-135">Поставщик не должен возвращать сведения об ошибке, если у него нет реализации указанного флага.</span><span class="sxs-lookup"><span data-stu-id="ef93f-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="ef93f-136">Результат ограничения содержимого, наложенного на свойство, не определено, если свойство не существует.</span><span class="sxs-lookup"><span data-stu-id="ef93f-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="ef93f-137">Когда клиенту требуется строго определенное поведение для такого ограничения, и не проверяется, существует ли это свойство например, это не обязательный столбец таблицы, он должен **создать ограничение для** присоединения к ограничению содержимого с ограничением EXISTS.</span><span class="sxs-lookup"><span data-stu-id="ef93f-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="ef93f-138">Используйте структуру [сексистрестриктион](sexistrestriction.md) , чтобы определить ограничение exist и структуру [сандрестриктион](sandrestriction.md) для **определения ограничения.**</span><span class="sxs-lookup"><span data-stu-id="ef93f-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="ef93f-139">Для получения дополнительных сведений о структуре и ограничениях **сконтентрестриктион** в целом ознакомьтесь с [ограничениями](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="ef93f-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef93f-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ef93f-140">See also</span></span>

- [<span data-ttu-id="ef93f-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ef93f-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="ef93f-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="ef93f-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="ef93f-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ef93f-143">MAPI Structures</span></span>](mapi-structures.md)

