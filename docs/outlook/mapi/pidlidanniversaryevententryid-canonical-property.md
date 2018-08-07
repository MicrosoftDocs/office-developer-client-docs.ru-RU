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
ms.openlocfilehash: 78096affce8fa03cc3efc8f0ca0c7048c2f9aae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810101"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="5010e-103">Каноническое свойство PidLidAnniversaryEventEntryId</span><span class="sxs-lookup"><span data-stu-id="5010e-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5010e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5010e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5010e-105">Указывает идентификатор записи встречи, представляющий Годовщина контакта.</span><span class="sxs-lookup"><span data-stu-id="5010e-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5010e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5010e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5010e-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="5010e-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="5010e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5010e-108">Property set:</span></span>  <br/> |<span data-ttu-id="5010e-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5010e-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5010e-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="5010e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5010e-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="5010e-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="5010e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5010e-112">Data type:</span></span>  <br/> |<span data-ttu-id="5010e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5010e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5010e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5010e-114">Area:</span></span>  <br/> |<span data-ttu-id="5010e-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="5010e-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5010e-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5010e-116">Remarks</span></span>

<span data-ttu-id="5010e-117">Встречи, указанного в свойстве **dispidAnniversaryEventEID** должен быть связан с этим контактом с помощью **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([ PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) и свойства **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), как описано в [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5010e-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5010e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5010e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5010e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5010e-119">Protocol specifications</span></span>

<span data-ttu-id="5010e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5010e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5010e-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5010e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5010e-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5010e-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5010e-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="5010e-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5010e-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5010e-124">Header files</span></span>

<span data-ttu-id="5010e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5010e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5010e-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5010e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5010e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5010e-127">See also</span></span>



[<span data-ttu-id="5010e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5010e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5010e-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5010e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5010e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5010e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5010e-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5010e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

