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
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="a40b5-103">Каноническое свойство PidTagSearchRecipientEmailCc</span><span class="sxs-lookup"><span data-stu-id="a40b5-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="a40b5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a40b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a40b5-105">Содержит строку Unicode, запрашиваемую в списке адресов электронной почты или отображает имена получателей, адресованных в строке **сообщений CC** в магазине.</span><span class="sxs-lookup"><span data-stu-id="a40b5-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="a40b5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a40b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a40b5-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="a40b5-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="a40b5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a40b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a40b5-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="a40b5-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="a40b5-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="a40b5-110">Property type:</span></span>  <br/> |<span data-ttu-id="a40b5-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a40b5-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a40b5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a40b5-112">Area:</span></span>  <br/> |<span data-ttu-id="a40b5-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="a40b5-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a40b5-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a40b5-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="a40b5-115">Этот тег ограничения MAPI, используемый при поиске адресов электронной почты или отображаемых имен, на которые отправляется сообщение в виде углеродной копии, может не быть определен в загружаемом файле загона, который у вас есть в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="a40b5-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="a40b5-116">Его можно добавить в код, используя следующее значение: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="a40b5-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="a40b5-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a40b5-117">Protocol specifications</span></span>

<span data-ttu-id="a40b5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a40b5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a40b5-119">Содержит ссылки на связанные Microsoft Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a40b5-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a40b5-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a40b5-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a40b5-121">Указывает свойства и операции для управления конфигурацией списка папки поиска.</span><span class="sxs-lookup"><span data-stu-id="a40b5-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a40b5-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a40b5-122">Header files</span></span>

<span data-ttu-id="a40b5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a40b5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a40b5-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a40b5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a40b5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a40b5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a40b5-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a40b5-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a40b5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a40b5-127">See also</span></span>



[<span data-ttu-id="a40b5-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a40b5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a40b5-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a40b5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a40b5-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a40b5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a40b5-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a40b5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

