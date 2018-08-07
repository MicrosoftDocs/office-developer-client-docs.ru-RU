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
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811291"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="09083-103">Каноническое свойство PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="09083-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="09083-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09083-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09083-105">Указывает, рассматриваются ли адреса электронной почты из контактов в папке контактов специально по отношению к фильтра нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="09083-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09083-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="09083-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09083-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="09083-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="09083-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="09083-108">Identifier:</span></span>  <br/> |<span data-ttu-id="09083-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="09083-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="09083-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="09083-110">Data type:</span></span>  <br/> |<span data-ttu-id="09083-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="09083-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="09083-112">Область:</span><span class="sxs-lookup"><span data-stu-id="09083-112">Area:</span></span>  <br/> |<span data-ttu-id="09083-113">Нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="09083-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09083-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="09083-114">Remarks</span></span>

<span data-ttu-id="09083-115">Если задано значение «0x00000001», эти адреса электронной почты необходимо заполнить части адреса электронной почты для связи «надежные» ограничении правило нежелательной электронной почты таким образом, чтобы сообщения от этих адресов обрабатывается как «не является нежелательным».</span><span class="sxs-lookup"><span data-stu-id="09083-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="09083-116">Если задано значение «0x00000000», адреса электронной почты из папки "Контакты" не добавляются в правило нежелательной электронной почты, а раздел правило должно быть значение NULL.</span><span class="sxs-lookup"><span data-stu-id="09083-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="09083-117">Если это свойство со значением «0x00000001» и, если добавлены контакт имеет адреса электронной почты, которые еще не включены в разделе надежные контакты правило нежелательной электронной почты, нужные адреса электронной почты необходимо добавить ограничения.</span><span class="sxs-lookup"><span data-stu-id="09083-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="09083-118">Если это свойство является «0x00000000», никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="09083-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="09083-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="09083-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09083-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="09083-120">Protocol specifications</span></span>

<span data-ttu-id="09083-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09083-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09083-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="09083-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09083-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09083-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09083-124">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="09083-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09083-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="09083-125">Header files</span></span>

<span data-ttu-id="09083-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09083-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="09083-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="09083-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="09083-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="09083-128">Mapitags.h</span></span>
  
> <span data-ttu-id="09083-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="09083-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09083-130">См. также</span><span class="sxs-lookup"><span data-stu-id="09083-130">See also</span></span>



[<span data-ttu-id="09083-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="09083-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09083-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="09083-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09083-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="09083-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09083-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="09083-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

