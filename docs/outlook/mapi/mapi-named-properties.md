---
title: Именованные свойства MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435049"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="be7a2-103">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be7a2-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="be7a2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be7a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be7a2-105">MAPI предоставляет средство для назначения имен свойствам, сопоставления этих имен с уникальными идентификаторами и для сохраняния этого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="be7a2-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="be7a2-106">Сохраняемое имя для сопоставления идентификаторов гарантирует, что имена свойств остаются действительными во всех сеансах.</span><span class="sxs-lookup"><span data-stu-id="be7a2-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="be7a2-107">Чтобы определить имя свойства, клиент или поставщик услуг составляет имя и хранит его в [структуре MAPINAMEID.](mapinameid.md)</span><span class="sxs-lookup"><span data-stu-id="be7a2-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="be7a2-108">Так как имена состоит из 32-битного глобально уникального идентификатора или GUID, а также строки символов Unicode или числового значения, создатели именных свойств могут создавать значимые имена, не опасаясь дублирования.</span><span class="sxs-lookup"><span data-stu-id="be7a2-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="be7a2-109">Имена уникальны, и их можно использовать без оценок их идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="be7a2-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="be7a2-110">Чтобы поддерживать названные свойства, поставщик служб реализует два метода : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — для перевода между именами и идентификаторами и для того, чтобы разрешить его методам [IMAPIProp:GetProps](imapiprop-getprops.md)[IMAPIProp:SetProps](imapiprop-setprops.md) для получения и изменения свойств с помощью идентификаторов в диапазоне именных свойств.</span><span class="sxs-lookup"><span data-stu-id="be7a2-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="be7a2-111">Диапазон именных идентификаторов свойств находится между 0x8000 и 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="be7a2-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="be7a2-112">Любой объект, реализуя **интерфейс IMAPIProp,** может поддерживать названные свойства.</span><span class="sxs-lookup"><span data-stu-id="be7a2-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="be7a2-113">Поставщики адресных книг, которые позволяют копировать записи других поставщиков в контейнеры и поставщики магазинов сообщений, которые могут использоваться для создания произвольных типов сообщений, необходимы для обеспечения этой поддержки.</span><span class="sxs-lookup"><span data-stu-id="be7a2-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="be7a2-114">Это вариант для всех других поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="be7a2-114">It is an option for all other service providers.</span></span> <span data-ttu-id="be7a2-115">Поставщики, которые не поддерживают именимые свойства, возвращают MAPI_E_NO_SUPPORT из методов **GetIDsFromNames** и **GetNamesFromIDs** и отказываются устанавливать свойства с идентификаторами 0x8000 или больше, возвращая MAPI_E_UNEXPECTED в **SPropProblemarray**.</span><span class="sxs-lookup"><span data-stu-id="be7a2-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="be7a2-116">Создание имен для свойств — это один из способов для клиентов определить новые свойства для существующих или настраиваемых классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="be7a2-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="be7a2-117">Поставщики услуг могут использовать свойства с именами для разоблачения уникальных функций своих систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="be7a2-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="be7a2-118">Еще одним использованием именных свойств является предоставление альтернативного способа ссылок на свойства с идентификаторами ниже 0x8000.</span><span class="sxs-lookup"><span data-stu-id="be7a2-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="be7a2-119">Например, клиент может использовать код, аналогичный следующему коду, чтобы получить имена для всех свойств объекта с именем:</span><span class="sxs-lookup"><span data-stu-id="be7a2-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

<span data-ttu-id="be7a2-120">Чтобы запросить все имена из набора свойств PS_PUBLIC_STRINGS, клиент заменит NULL в параметре набора свойств на PS_PUBLIC_STRINGS следующим образом:</span><span class="sxs-lookup"><span data-stu-id="be7a2-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a><span data-ttu-id="be7a2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="be7a2-121">See also</span></span>

- [<span data-ttu-id="be7a2-122">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="be7a2-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

