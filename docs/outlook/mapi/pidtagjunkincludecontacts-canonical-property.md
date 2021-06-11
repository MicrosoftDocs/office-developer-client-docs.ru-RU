---
title: Каноническое свойство PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328716"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="cd1bd-103">Каноническое свойство PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="cd1bd-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="cd1bd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd1bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd1bd-105">Указывает, обрабатываются ли адреса электронной почты контактов в папке Contacts специально в отношении фильтра нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd1bd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cd1bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd1bd-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="cd1bd-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="cd1bd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cd1bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd1bd-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="cd1bd-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="cd1bd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cd1bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd1bd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cd1bd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cd1bd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cd1bd-112">Area:</span></span>  <br/> |<span data-ttu-id="cd1bd-113">Спам</span><span class="sxs-lookup"><span data-stu-id="cd1bd-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd1bd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd1bd-114">Remarks</span></span>

<span data-ttu-id="cd1bd-115">Если установлено "0x00000001", эти адреса электронной почты должны заполнять "доверенный" адрес электронной почты в части ограничения правил нежелательной почты, чтобы почта с этих адресов относилась к "не нежелательной".</span><span class="sxs-lookup"><span data-stu-id="cd1bd-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="cd1bd-116">Если установлено "0x00000000", адреса электронной почты из папки "Контакты" не должны быть добавлены в правило нежелательной почты, а раздел правила должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="cd1bd-117">Если это свойство имеет значение "0x00000001" и если у добавленного контакта есть адреса электронной почты, которые еще не включены в раздел доверенных контактов правила нежелательной электронной почты, эти адреса электронной почты должны быть добавлены в ограничение.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="cd1bd-118">Если это свойство "0x00000000", никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd1bd-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cd1bd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd1bd-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cd1bd-120">Protocol specifications</span></span>

<span data-ttu-id="cd1bd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd1bd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd1bd-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd1bd-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd1bd-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd1bd-124">Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd1bd-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="cd1bd-125">Header files</span></span>

<span data-ttu-id="cd1bd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd1bd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd1bd-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd1bd-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd1bd-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cd1bd-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="cd1bd-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd1bd-130">См. также</span><span class="sxs-lookup"><span data-stu-id="cd1bd-130">See also</span></span>



[<span data-ttu-id="cd1bd-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cd1bd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd1bd-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cd1bd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd1bd-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cd1bd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd1bd-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="cd1bd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

