---
title: Каноническое свойство PidLidContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2a097b8e8071c08b82a05f3c8e0b021db8ec5107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585397"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="13f47-103">Каноническое свойство PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="13f47-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="13f47-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13f47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13f47-105">Содержит имена контактов, связанный с элементом.</span><span class="sxs-lookup"><span data-stu-id="13f47-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13f47-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="13f47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13f47-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="13f47-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="13f47-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="13f47-108">Property set:</span></span>  <br/> |<span data-ttu-id="13f47-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="13f47-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="13f47-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="13f47-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13f47-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="13f47-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="13f47-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="13f47-112">Data type:</span></span>  <br/> |<span data-ttu-id="13f47-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13f47-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13f47-114">Область:</span><span class="sxs-lookup"><span data-stu-id="13f47-114">Area:</span></span>  <br/> |<span data-ttu-id="13f47-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="13f47-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13f47-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="13f47-116">Remarks</span></span>

<span data-ttu-id="13f47-117">Это свойство содержит свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) каждого адресной книги **EntryID** , который содержит ссылку на значение свойства **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="13f47-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="13f47-118">Она может включать имена, не **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="13f47-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13f47-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13f47-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13f47-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="13f47-120">Protocol specifications</span></span>

<span data-ttu-id="13f47-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f47-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f47-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13f47-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13f47-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f47-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f47-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="13f47-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="13f47-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f47-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f47-126">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="13f47-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="13f47-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f47-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f47-128">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="13f47-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13f47-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="13f47-129">Header files</span></span>

<span data-ttu-id="13f47-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13f47-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="13f47-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="13f47-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13f47-132">См. также</span><span class="sxs-lookup"><span data-stu-id="13f47-132">See also</span></span>



[<span data-ttu-id="13f47-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13f47-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13f47-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13f47-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13f47-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="13f47-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13f47-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="13f47-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

