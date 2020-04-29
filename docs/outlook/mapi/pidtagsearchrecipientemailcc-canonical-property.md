---
title: Каноническое свойство PidTagSearchRecipientEmailCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358949"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="7c384-103">Каноническое свойство PidTagSearchRecipientEmailCc</span><span class="sxs-lookup"><span data-stu-id="7c384-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="7c384-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c384-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c384-105">Содержит строку Юникода, запрашиваемую в списке адресов электронной почты или отображаемых имен получателей, которые адресованы в строке **"копия"** сообщений в магазине.</span><span class="sxs-lookup"><span data-stu-id="7c384-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7c384-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7c384-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c384-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="7c384-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="7c384-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7c384-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c384-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="7c384-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="7c384-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="7c384-110">Property type:</span></span>  <br/> |<span data-ttu-id="7c384-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c384-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7c384-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7c384-112">Area:</span></span>  <br/> |<span data-ttu-id="7c384-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="7c384-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7c384-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7c384-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="7c384-115">Этот тег ограничения MAPI используется при поиске адресов электронной почты или отображаемых имен, в которые сообщение отправляется в виде копии, может не быть определено в файле заголовков, которые есть у вас в данный момент.</span><span class="sxs-lookup"><span data-stu-id="7c384-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="7c384-116">Вы можете добавить его в код, используя следующее значение: >`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="7c384-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="7c384-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7c384-117">Protocol specifications</span></span>

<span data-ttu-id="7c384-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c384-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c384-119">Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7c384-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c384-120">[[MS — ОКСОСРЧ]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c384-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c384-121">Задает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="7c384-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c384-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7c384-122">Header files</span></span>

<span data-ttu-id="7c384-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7c384-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c384-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7c384-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c384-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="7c384-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7c384-126">Содержит определения свойств, которые перечислены как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="7c384-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c384-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7c384-127">See also</span></span>



[<span data-ttu-id="7c384-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7c384-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c384-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="7c384-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c384-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7c384-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c384-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7c384-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

