---
title: Теги свойства MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390018"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="a858b-103">Теги свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a858b-103">MAPI property tags</span></span>
  
<span data-ttu-id="a858b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a858b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a858b-105">Свойство tag — это 32-разрядное число, которое содержит уникальный идентификатор в битах 16 до 31 и тип свойства в битах цифры от 0 до 15, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="a858b-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="a858b-106">**Элементы тега свойства**</span><span class="sxs-lookup"><span data-stu-id="a858b-106">**Property tag elements**</span></span>
  
<span data-ttu-id="a858b-107">![Элементы тега свойства] (media/amapi_10.gif "Элементы тега свойства")</span><span class="sxs-lookup"><span data-stu-id="a858b-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="a858b-108">Свойство теги используются для определения свойства MAPI, и каждое свойство должно иметь одну, независимо от того, является ли свойство определяется MAPI, клиента или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a858b-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="a858b-109">MAPI определяет набор свойств тега константы для его свойства в файле заголовка Mapitags.h; Эти свойства будут называться «определенные MAPI свойств».</span><span class="sxs-lookup"><span data-stu-id="a858b-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="a858b-110">Свойство tag константы следуйте соглашение об именовании для согласованности и удобства использования.</span><span class="sxs-lookup"><span data-stu-id="a858b-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="a858b-111">Имя каждого свойства tag на две части: префикс PR_ и один или несколько строк символов, которые описывают содержимое свойства.</span><span class="sxs-lookup"><span data-stu-id="a858b-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="a858b-112">Несколько строк символов, разделенных подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="a858b-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="a858b-113">Например, свойство tag для типа адреса получателя сообщения будет **связей с Общественностью\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) и **PR_IPM_SENTMAIL_ — это идентификатор записи для папки, предназначенный для получения копии всех исходящих сообщений Идентификатор записи** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a858b-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="a858b-114">Несколько макросов, доступны для работы с тегами свойство, между ними [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)и [PROP_TAG](prop_tag.md).</span><span class="sxs-lookup"><span data-stu-id="a858b-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="a858b-115">**СВОЙСТВА\_тип** извлекает тип свойства из тега свойства; **Свойства\_идентификатор** извлекает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a858b-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="a858b-116">**PROP_TAG** построения тега свойства из типа свойства и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a858b-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a858b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a858b-117">See also</span></span>

- [<span data-ttu-id="a858b-118">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="a858b-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

