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
# <a name="handling-named-property-errors"></a><span data-ttu-id="8ad4f-103">Обработка ошибок именованных свойств</span><span class="sxs-lookup"><span data-stu-id="8ad4f-103">Handling named property errors</span></span>
  
<span data-ttu-id="8ad4f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ad4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ad4f-105">При выполнении запроса к [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs,](imapiprop-getnamesfromids.md) которое слишком большое для реализации, возвращается значение MAPI_E_TOO_BIG ошибки.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-105">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned.</span></span> <span data-ttu-id="8ad4f-106">Вызывающие должны разделить свой запрос на несколько запросов, вызывая соответствующий метод в цикле.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-106">Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="8ad4f-107">Если вызов приводит к частичному успеху, например когда запрос касается имен, которые соотнесются с определенными идентификаторами и не удается найти одно или несколько имен, **GetNamesFromIDs** возвращает MAPI_W_ERRORS_RETURNED и помещает PT_ERROR в тип свойства для отсутствующих свойств в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="8ad4f-108">Иногда клиент совершает вызов **GetNamesFromIDs,** что приводит к неудажным свойствам, таким как отсутствие свойств в указанном наборе свойств или когда все именуемые свойства имеют тип, исключенный флагами.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-108">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags.</span></span> <span data-ttu-id="8ad4f-109">Клиенты могут ожидать от поставщиков услуг:</span><span class="sxs-lookup"><span data-stu-id="8ad4f-109">Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="8ad4f-110">Возврат S_OK.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-110">Return S_OK.</span></span>
    
- <span data-ttu-id="8ad4f-111">Установите для содержимого указателя массива тегов свойств только что выделенный массив тегов свойств, для его члена **cValues** установлено нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="8ad4f-112">Установите для содержимого массива [структуры MAPINAMEID](mapinameid.md) NULL.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="8ad4f-113">Задайте для содержимого подсчета структур **MAPINAMEID** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8ad4f-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8ad4f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8ad4f-114">See also</span></span>

- [<span data-ttu-id="8ad4f-115">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad4f-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

