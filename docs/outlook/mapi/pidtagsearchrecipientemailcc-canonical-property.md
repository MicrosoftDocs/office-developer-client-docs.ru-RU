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
ms.openlocfilehash: 6ac54e5a17c17ea36ededd311d55c52ece0c184e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572608"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="bc5b0-103">Каноническое свойство PidTagSearchRecipientEmailCc</span><span class="sxs-lookup"><span data-stu-id="bc5b0-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="bc5b0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc5b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc5b0-105">Содержит строку Юникод, запрашиваемый в список адресов электронной почты или отображаемые имена получателей, которые описываются в строке **копия** сообщения в хранилище.</span><span class="sxs-lookup"><span data-stu-id="bc5b0-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="bc5b0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bc5b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc5b0-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="bc5b0-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="bc5b0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bc5b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc5b0-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="bc5b0-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="bc5b0-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="bc5b0-110">Property type:</span></span>  <br/> |<span data-ttu-id="bc5b0-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc5b0-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bc5b0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bc5b0-112">Area:</span></span>  <br/> |<span data-ttu-id="bc5b0-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="bc5b0-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bc5b0-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bc5b0-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="bc5b0-115">Этот тег ограничений MAPI, используемый при выполнении поиска для адресов электронной почты или отображаемые имена, к которым сообщение отправляется как скрытую копию не могут быть определены в файле загружаемых заголовка, который в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="bc5b0-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="bc5b0-116">Добавьте в код с помощью следующее значение: >`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="bc5b0-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="bc5b0-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bc5b0-117">Protocol specifications</span></span>

<span data-ttu-id="bc5b0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc5b0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc5b0-119">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bc5b0-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc5b0-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc5b0-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc5b0-121">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="bc5b0-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc5b0-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bc5b0-122">Header files</span></span>

<span data-ttu-id="bc5b0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc5b0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc5b0-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bc5b0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc5b0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc5b0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bc5b0-126">Содержит определения свойства, указанные как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="bc5b0-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc5b0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bc5b0-127">See also</span></span>



[<span data-ttu-id="bc5b0-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bc5b0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc5b0-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bc5b0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc5b0-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bc5b0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc5b0-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bc5b0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

