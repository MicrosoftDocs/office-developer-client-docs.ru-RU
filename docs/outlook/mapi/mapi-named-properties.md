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
ms.openlocfilehash: e755c18ef3cc32f9a00169f19cf336eace447a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809779"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="9a51e-103">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9a51e-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="9a51e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a51e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a51e-105">MAPI предоставляет средства для назначения имен свойств, для сопоставления этих имен с уникальными идентификаторами и предъявления сохраняемого это сопоставление.</span><span class="sxs-lookup"><span data-stu-id="9a51e-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="9a51e-106">Постоянное имя для сопоставления идентификатора гарантирует, что имена свойств остаются действительными между сеансами.</span><span class="sxs-lookup"><span data-stu-id="9a51e-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="9a51e-107">Определение именованного свойства клиента или поставщика делает название и сохраняет его в структуре [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="9a51e-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="9a51e-108">Поскольку имена состоят из 32-разрядная версия глобальный уникальный идентификатор, или идентификатор GUID и либо значение символа Юникода строковые или числовые, создателей именованных свойств можно создать понятные имена не копирования.</span><span class="sxs-lookup"><span data-stu-id="9a51e-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="9a51e-109">Имена являются уникальными и они могут использоваться независимо от значения идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="9a51e-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="9a51e-110">Чтобы обеспечить поддержку именованных свойств, поставщик службы реализует два метода — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — для перевода между имена и идентификаторы и разрешить его [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) методы для получения и изменение свойств с идентификаторами в диапазоне именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="9a51e-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="9a51e-111">Значения идентификаторов именованного свойства — от 0x8000 до 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="9a51e-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="9a51e-112">Любой объект, реализующий интерфейс **IMAPIProp** может поддерживать именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="9a51e-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="9a51e-113">Поставщиками адресных книг, поддерживающих записи от других поставщиков копируются в своих сообщений и контейнеры хранения поставщиков, которые могут использоваться для создания типов сообщений произвольных необходимы для предоставления этой поддержки.</span><span class="sxs-lookup"><span data-stu-id="9a51e-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="9a51e-114">Он может использоваться для других поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="9a51e-114">It is an option for all other service providers.</span></span> <span data-ttu-id="9a51e-115">Поставщики, которые не поддерживают именованные свойства возврата MAPI_E_NO_SUPPORT из методов **GetIDsFromNames** и **GetNamesFromIDs** и не будет задайте свойства с идентификаторами 0x8000 или более высокой версии, возвращает ошибку MAPI_E_UNEXPECTED в ** SPropProblemarray**.</span><span class="sxs-lookup"><span data-stu-id="9a51e-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="9a51e-116">Создание имен для свойства является одним из способов для клиентов определить новые свойства для существующего или пользовательских классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="9a51e-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="9a51e-117">Поставщиков услуг можно использовать именованные свойства для предоставления уникальных функций их систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9a51e-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="9a51e-118">Пока другой именованных свойств используется для предоставления альтернативного способа ссылок на свойства с идентификаторами ниже 0x8000.</span><span class="sxs-lookup"><span data-stu-id="9a51e-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="9a51e-119">Например клиент может использовать код, похожий на следующий код для извлечения имен для всех именованных свойств объекта:</span><span class="sxs-lookup"><span data-stu-id="9a51e-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="9a51e-120">Чтобы запросить все имена PS_PUBLIC_STRINGS набор свойств, клиент заменить NULL в параметре set свойства PS_PUBLIC_STRINGS следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9a51e-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9a51e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9a51e-121">See also</span></span>

- [<span data-ttu-id="9a51e-122">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="9a51e-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

