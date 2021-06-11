---
title: Обработка ошибок именованных свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 98b6adbc3a31994768a78b389e16eb3a6ece34bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429868"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="0cc8c-103">Обработка ошибок именованных свойств</span><span class="sxs-lookup"><span data-stu-id="0cc8c-103">Handling named property errors</span></span>
  
<span data-ttu-id="0cc8c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cc8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cc8c-105">При запросе на [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs,](imapiprop-getnamesfromids.md) которые слишком большие для выполнения, возвращается значение MAPI_E_TOO_BIG ошибки.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-105">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned.</span></span> <span data-ttu-id="0cc8c-106">Звонители должны разделить запрос на несколько запросов, назвав соответствующий метод в цикле.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-106">Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="0cc8c-107">Если вызов приводит к частичному успеху, например если запрос на имена, которые соотносят с определенными идентификаторами, и не удается найти одно или несколько имен, **GetNamesFromID возвращает** MAPI_W_ERRORS_RETURNED и помещает PT_ERROR в тип свойства для отсутствующих свойств в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="0cc8c-108">Иногда клиент звонит в **GetNamesFromIDs,** в результате чего свойства не возвращаются, например, когда в указанном наборе свойств нет свойств, или когда все указанные свойства имеют тип, исключаемый флагами.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-108">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags.</span></span> <span data-ttu-id="0cc8c-109">Клиенты могут ожидать от поставщиков услуг:</span><span class="sxs-lookup"><span data-stu-id="0cc8c-109">Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="0cc8c-110">Возвращение S_OK.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-110">Return S_OK.</span></span>
    
- <span data-ttu-id="0cc8c-111">Установите содержимое указателя массива тегов свойств в недавно выделенный массив тегов свойств с его **членом cValues,** заниженным до нуля.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="0cc8c-112">Установите содержимое массива [структуры MAPINAMEID](mapinameid.md) nULL.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="0cc8c-113">Установите значение содержимого для подсчета структур **MAPINAMEID** до нуля.</span><span class="sxs-lookup"><span data-stu-id="0cc8c-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0cc8c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0cc8c-114">See also</span></span>

- [<span data-ttu-id="0cc8c-115">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0cc8c-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

