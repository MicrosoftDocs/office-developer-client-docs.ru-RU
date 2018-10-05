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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399629"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="14856-103">Каноническое свойство PidLidAnniversaryEventEntryId</span><span class="sxs-lookup"><span data-stu-id="14856-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="14856-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14856-105">Указывает идентификатор записи встречи, представляющий Годовщина контакта.</span><span class="sxs-lookup"><span data-stu-id="14856-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14856-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="14856-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14856-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="14856-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="14856-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="14856-108">Property set:</span></span>  <br/> |<span data-ttu-id="14856-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="14856-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="14856-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="14856-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="14856-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="14856-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="14856-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="14856-112">Data type:</span></span>  <br/> |<span data-ttu-id="14856-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="14856-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="14856-114">Область:</span><span class="sxs-lookup"><span data-stu-id="14856-114">Area:</span></span>  <br/> |<span data-ttu-id="14856-115">Contact</span><span class="sxs-lookup"><span data-stu-id="14856-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14856-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="14856-116">Remarks</span></span>

<span data-ttu-id="14856-117">Встречи, указанного в свойстве **dispidAnniversaryEventEID** должен быть связан с этим контактом с помощью **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([ PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) и свойства **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), как описано в [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="14856-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14856-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="14856-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14856-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="14856-119">Protocol specifications</span></span>

<span data-ttu-id="14856-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14856-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14856-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="14856-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14856-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14856-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14856-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="14856-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14856-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="14856-124">Header files</span></span>

<span data-ttu-id="14856-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14856-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="14856-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="14856-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14856-127">См. также</span><span class="sxs-lookup"><span data-stu-id="14856-127">See also</span></span>



[<span data-ttu-id="14856-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14856-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14856-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14856-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14856-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="14856-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14856-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="14856-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

