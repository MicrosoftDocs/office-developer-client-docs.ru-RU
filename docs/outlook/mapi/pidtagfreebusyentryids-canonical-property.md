---
title: Каноническое свойство PidTagFreeBusyEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyEntryIds
api_type:
- HeaderDef
ms.assetid: 8bc40ebf-76f2-49dd-af4b-4095bc07c639
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0feaac0cb4c52b2f2acff1460a4d8a41196954d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811178"
---
# <a name="pidtagfreebusyentryids-canonical-property"></a><span data-ttu-id="608c6-103">Каноническое свойство PidTagFreeBusyEntryIds</span><span class="sxs-lookup"><span data-stu-id="608c6-103">PidTagFreeBusyEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="608c6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="608c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="608c6-105">Содержит **EntryIDs** для сообщения сведения делегата, сообщения о доступности пользователя, выполнившего вход и папки, чьи **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) равен «Занятости данных».</span><span class="sxs-lookup"><span data-stu-id="608c6-105">Contains the **EntryIDs** for the delegate information message, the free/busy message of the logged in user, and the folder whose **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) is equal to "FreeBusy Data."</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="608c6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="608c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="608c6-107">PR_FREEBUSY_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="608c6-107">PR_FREEBUSY_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="608c6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="608c6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="608c6-109">0x36E4</span><span class="sxs-lookup"><span data-stu-id="608c6-109">0x36E4</span></span>  <br/> |
|<span data-ttu-id="608c6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="608c6-110">Data type:</span></span>  <br/> |<span data-ttu-id="608c6-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="608c6-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="608c6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="608c6-112">Area:</span></span>  <br/> |<span data-ttu-id="608c6-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="608c6-113">MAPI container</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="608c6-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="608c6-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="608c6-115">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="608c6-115">Protocol specifications</span></span>

<span data-ttu-id="608c6-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="608c6-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="608c6-117">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="608c6-117">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="608c6-118">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="608c6-118">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="608c6-119">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="608c6-119">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="608c6-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="608c6-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="608c6-121">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с элементами календаря и сообщения, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="608c6-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="608c6-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="608c6-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="608c6-123">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="608c6-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="608c6-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="608c6-124">Header files</span></span>

<span data-ttu-id="608c6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="608c6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="608c6-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="608c6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="608c6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="608c6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="608c6-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="608c6-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="608c6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="608c6-129">See also</span></span>



[<span data-ttu-id="608c6-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="608c6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="608c6-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="608c6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="608c6-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="608c6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="608c6-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="608c6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

