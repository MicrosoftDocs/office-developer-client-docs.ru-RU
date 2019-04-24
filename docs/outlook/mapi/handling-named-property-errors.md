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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299372"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="9a55b-103">Обработка ошибок именованных свойств</span><span class="sxs-lookup"><span data-stu-id="9a55b-103">Handling named property errors</span></span>
  
<span data-ttu-id="9a55b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a55b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a55b-105">При выполнении запроса к [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) или [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) , который слишком велик для обработки разработчиком, возвращается значение ошибки мапи_е_ту_биг.</span><span class="sxs-lookup"><span data-stu-id="9a55b-105">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned.</span></span> <span data-ttu-id="9a55b-106">Абоненты должны разделить свой запрос на несколько запросов, вызывая соответствующий метод в цикле.</span><span class="sxs-lookup"><span data-stu-id="9a55b-106">Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="9a55b-107">Когда вызов вызывает частичное успешное выполнение, например, когда запрос предназначен для имен, которые сопоставляются с определенными идентификаторами, и не удается найти одно или несколько имен, **жетнамесфромидс** возвращает мапи_в_еррорс_ретурнед и помещает пт_еррор в тип свойства для отсутствующего в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="9a55b-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="9a55b-108">Иногда клиент выполняет вызов **жетнамесфромидс** , в результате чего не возвращаются свойства, например при отсутствии свойств в указанном наборе свойств или если все именованные свойства имеют тип, исключенный с помощью флагов.</span><span class="sxs-lookup"><span data-stu-id="9a55b-108">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags.</span></span> <span data-ttu-id="9a55b-109">Клиенты могут ожидать от поставщиков услуг:</span><span class="sxs-lookup"><span data-stu-id="9a55b-109">Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="9a55b-110">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="9a55b-110">Return S_OK.</span></span>
    
- <span data-ttu-id="9a55b-111">Задайте для содержимого указателя массива тегов свойств новый выделенный массив тегов свойств с набором элементов **квалуес** , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="9a55b-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="9a55b-112">Задайте для содержимого массива структуры [МАПИНАМЕИД](mapinameid.md) значение null.</span><span class="sxs-lookup"><span data-stu-id="9a55b-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="9a55b-113">Задайте для содержимого счетчика **мапинамеид** значение ноль.</span><span class="sxs-lookup"><span data-stu-id="9a55b-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9a55b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9a55b-114">See also</span></span>

- [<span data-ttu-id="9a55b-115">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9a55b-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

