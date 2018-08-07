---
title: Свойство ошибки с именем обработки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9ea1c4063c08844052618c50fe53fdc0064787a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808562"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="129fb-103">Свойство ошибки с именем обработки</span><span class="sxs-lookup"><span data-stu-id="129fb-103">Handling named property errors</span></span>
  
<span data-ttu-id="129fb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="129fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="129fb-105">При запросе [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или слишком велик для реализации обработки [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) MAPI_E_TOO_BIG возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="129fb-105">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned.</span></span> <span data-ttu-id="129fb-106">Абонентов необходимо разделить свой запрос на несколько запросов вызова соответствующего метода в цикле.</span><span class="sxs-lookup"><span data-stu-id="129fb-106">Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="129fb-107">Если не удается найти результаты вызовов в частичное успешно, например, когда запрос для имен, которые сопоставляют определенные идентификаторы и одно или несколько имен, **GetNamesFromIDs** возвращает MAPI_W_ERRORS_RETURNED и помещает PT_ERROR в тип свойства для отсутствующих свойство в массиве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="129fb-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="129fb-108">В некоторых случаях клиент вызывает **GetNamesFromIDs** , которая приводит к нет свойств, возвращаемых, например, когда нет свойств в наборе указанное свойство, или когда все именованные свойства типа исключены с флаги.</span><span class="sxs-lookup"><span data-stu-id="129fb-108">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags.</span></span> <span data-ttu-id="129fb-109">Клиенты могут ожидать поставщиков услуг для:</span><span class="sxs-lookup"><span data-stu-id="129fb-109">Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="129fb-110">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="129fb-110">Return S_OK.</span></span>
    
- <span data-ttu-id="129fb-111">Значение массива тег вновь выделенный свойства содержимое указателя свойство tag массива с его элементом **cValues** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="129fb-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="129fb-112">Содержимое массива структура [MAPINAMEID](mapinameid.md) значение NULL.</span><span class="sxs-lookup"><span data-stu-id="129fb-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="129fb-113">Задайте содержимое числа структур **MAPINAMEID** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="129fb-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="129fb-114">См. также</span><span class="sxs-lookup"><span data-stu-id="129fb-114">See also</span></span>

- [<span data-ttu-id="129fb-115">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="129fb-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

