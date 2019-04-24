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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345866"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="9345f-103">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9345f-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="9345f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9345f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9345f-105">MAPI позволяет назначать имена свойствам для сопоставления этих имен с уникальными идентификаторами, а также для сохранения этого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9345f-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="9345f-106">Постоянное имя с сопоставлением идентификаторов гарантирует, что имена свойств оставались допустимыми в сеансах.</span><span class="sxs-lookup"><span data-stu-id="9345f-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="9345f-107">Чтобы определить именованное свойство, клиент или поставщик услуг образует имя и сохраняет его в структуре [мапинамеид](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="9345f-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="9345f-108">Поскольку имена состоят из 32-разрядного глобального уникального идентификатора (GUID), а также строки символов Юникода или числового значения, создатели именованных свойств могут создавать осмысленные имена, не опасаясь дублирования.</span><span class="sxs-lookup"><span data-stu-id="9345f-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="9345f-109">Имена являются уникальными и могут использоваться без учета значений их идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="9345f-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="9345f-110">Для поддержки именованных свойств поставщик услуг реализует два метода — [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) и [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) — для преобразования между именами и идентификаторами, а также для разрешения [IMAPIProp::-PROPS](imapiprop-getprops.md) [ IMAPIProp:: SetProps](imapiprop-setprops.md) методы для получения и изменения свойств с идентификаторами в именованном диапазоне свойств.</span><span class="sxs-lookup"><span data-stu-id="9345f-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="9345f-111">Диапазон именованных идентификаторов свойств находится в пределах от 0x8000 до 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="9345f-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="9345f-112">Любой объект, реализующий интерфейс **IMAPIProp** , может поддерживать именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9345f-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="9345f-113">Поставщики адресных книг, которые позволяют копировать записи от других поставщиков в контейнеры и поставщики хранилища сообщений, которые можно использовать для создания произвольных типов сообщений, для предоставления этой поддержки.</span><span class="sxs-lookup"><span data-stu-id="9345f-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="9345f-114">Это параметр для всех других поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="9345f-114">It is an option for all other service providers.</span></span> <span data-ttu-id="9345f-115">Поставщики, не поддерживающие именованные свойства, возвращают МАПИ_Е_НО_СУППОРТ из методов **жетидсфромнамес** и **жетнамесфромидс** и отклоняют свойства с идентификаторами от 0x8000 и выше, возвращая мапи_е_унекспектед в **методе Спроппроблемаррай**.</span><span class="sxs-lookup"><span data-stu-id="9345f-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="9345f-116">Создание имен для свойств — это один способ для клиентов определять новые свойства для существующих или настраиваемых классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="9345f-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="9345f-117">Поставщики услуг могут использовать именованные свойства для предоставления уникальных функций систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9345f-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="9345f-118">Но еще один способ использовать именованные свойства — предоставить альтернативный способ обращения к свойствам с идентификаторами ниже 0x8000.</span><span class="sxs-lookup"><span data-stu-id="9345f-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="9345f-119">Например, клиент может использовать код, похожий на приведенный ниже код, для получения имен всех именованных свойств объекта:</span><span class="sxs-lookup"><span data-stu-id="9345f-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="9345f-120">Чтобы запросить все имена из набора свойств ПС_ПУБЛИК_СТРИНГС, клиент заменит значение NULL в параметре Set свойства на ПС_ПУБЛИК_СТРИНГС следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9345f-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9345f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9345f-121">See also</span></span>

- [<span data-ttu-id="9345f-122">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="9345f-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

