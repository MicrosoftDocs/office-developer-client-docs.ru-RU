---
title: Каноническое свойство PidLidAnniversaryEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335576"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="9210f-103">Каноническое свойство PidLidAnniversaryEventEntryId</span><span class="sxs-lookup"><span data-stu-id="9210f-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9210f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9210f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9210f-105">Указывает идентификатор записи встречи, которая представляет годовщину контакта.</span><span class="sxs-lookup"><span data-stu-id="9210f-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9210f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9210f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9210f-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="9210f-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="9210f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9210f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9210f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9210f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9210f-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="9210f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9210f-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="9210f-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="9210f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9210f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9210f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9210f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9210f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9210f-114">Area:</span></span>  <br/> |<span data-ttu-id="9210f-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="9210f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9210f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9210f-116">Remarks</span></span>

<span data-ttu-id="9210f-117">Встреча, указанная свойством **dispidAnniversaryEventEID,** должна быть связана с этим контактом с помощью свойств **dispidContactLinkEntry** ([PidLidContactLinkEntry),](pidlidcontactlinkentry-canonical-property.md) **dispidContactLinkSearchKey** [(PidLidContactLinkSearchKey)](pidlidcontactlinksearchkey-canonical-property.md)и **dispidContactLinkName** ([PidLidContactLinkName),](pidlidcontactlinkname-canonical-property.md)как описано [в [MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9210f-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9210f-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9210f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9210f-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9210f-119">Protocol specifications</span></span>

<span data-ttu-id="9210f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9210f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9210f-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="9210f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9210f-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9210f-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9210f-123">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="9210f-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9210f-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="9210f-124">Header files</span></span>

<span data-ttu-id="9210f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9210f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9210f-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9210f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9210f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9210f-127">See also</span></span>



[<span data-ttu-id="9210f-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9210f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9210f-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9210f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9210f-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9210f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9210f-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9210f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

