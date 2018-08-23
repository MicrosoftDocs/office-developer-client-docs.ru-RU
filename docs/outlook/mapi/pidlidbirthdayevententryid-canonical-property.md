---
title: Каноническое свойство PidLidBirthdayEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7d8a142729d1c86c615653b2cbfc708268d4322e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576780"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="19187-103">Каноническое свойство PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="19187-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="19187-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19187-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19187-105">Указывает **идентификатор записи** необязательно встречи, представляющий день рождения контакта.</span><span class="sxs-lookup"><span data-stu-id="19187-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19187-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="19187-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19187-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="19187-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="19187-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="19187-108">Property set:</span></span>  <br/> |<span data-ttu-id="19187-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="19187-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="19187-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="19187-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="19187-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="19187-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="19187-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="19187-112">Data type:</span></span>  <br/> |<span data-ttu-id="19187-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="19187-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="19187-114">Область:</span><span class="sxs-lookup"><span data-stu-id="19187-114">Area:</span></span>  <br/> |<span data-ttu-id="19187-115">Contact</span><span class="sxs-lookup"><span data-stu-id="19187-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19187-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="19187-116">Remarks</span></span>

<span data-ttu-id="19187-117">Встречи, это заданный этим свойством должен быть связан с этим контактом с помощью **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) и ** dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) свойства, как указано в [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="19187-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="19187-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="19187-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19187-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="19187-119">Protocol specifications</span></span>

<span data-ttu-id="19187-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19187-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19187-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="19187-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19187-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19187-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19187-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="19187-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19187-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="19187-124">Header files</span></span>

<span data-ttu-id="19187-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19187-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="19187-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="19187-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19187-127">См. также</span><span class="sxs-lookup"><span data-stu-id="19187-127">See also</span></span>



[<span data-ttu-id="19187-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19187-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19187-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19187-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19187-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="19187-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19187-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="19187-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

