---
title: Теги свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328240"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="3fe4d-103">Теги свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="3fe4d-103">MAPI property tags</span></span>
  
<span data-ttu-id="3fe4d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fe4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fe4d-105">Тег свойства — это 32-битный номер, содержащий уникальный идентификатор свойства в битах от 16 до 31 и тип свойства в битах от 0 до 15, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="3fe4d-106">**Элементы тега свойства**</span><span class="sxs-lookup"><span data-stu-id="3fe4d-106">**Property tag elements**</span></span>
  
<span data-ttu-id="3fe4d-107">![Элементы тега свойства Элементы](media/amapi_10.gif "тегов Свойства")</span><span class="sxs-lookup"><span data-stu-id="3fe4d-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="3fe4d-108">Теги свойств используются для определения свойств MAPI, и каждое свойство должно иметь одно, независимо от того, определяется ли свойство MAPI, клиентом или поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="3fe4d-109">MAPI определяет набор констант тегов свойств для его свойств в файле загона Mapitags.h; эти свойства называются "свойствами, определенными mapI".</span><span class="sxs-lookup"><span data-stu-id="3fe4d-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="3fe4d-110">Константы тегов свойств следуют конвенции именования для последовательности и простоты использования.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="3fe4d-111">В названии каждого тега свойств есть две части: префикс PR_ и одна или несколько строк символов, описывающие содержимое свойства.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="3fe4d-112">Несколько строк символов разделены подчеркнутами.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="3fe4d-113">Например, тег свойства для типа адреса получателя сообщения — PR **\_ ADDRTYPE** [(PidTagOrgAddrtype),](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)а идентификатором входа для папки, назначенной для получения копии каждого исходящие сообщения, является **PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId).](pidtagipmsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3fe4d-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="3fe4d-114">Для работы с тегами свойств доступны несколько макрос, среди которых [PROP_TYPE,](prop_type.md) [PROP_ID](prop_id.md)и [PROP_TAG.](prop_tag.md)</span><span class="sxs-lookup"><span data-stu-id="3fe4d-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="3fe4d-115">**PROP \_ TYPE** извлекает тип свойства из тега свойства; **PROP \_ Идентификатор извлекает** идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="3fe4d-116">**PROP_TAG** создает тег свойства из типа свойства и идентификатора.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3fe4d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3fe4d-117">See also</span></span>

- [<span data-ttu-id="3fe4d-118">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="3fe4d-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

