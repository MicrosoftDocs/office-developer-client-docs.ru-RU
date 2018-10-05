---
title: Каноническое свойство PidTag7BitDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401071"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="9e6b2-103">Каноническое свойство PidTag7BitDisplayName</span><span class="sxs-lookup"><span data-stu-id="9e6b2-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9e6b2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e6b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e6b2-105">Содержит представление ASCII 7-битовое имя системы обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e6b2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9e6b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e6b2-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9e6b2-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9e6b2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9e6b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e6b2-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="9e6b2-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="9e6b2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9e6b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e6b2-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e6b2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9e6b2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9e6b2-112">Area:</span></span>  <br/> |<span data-ttu-id="9e6b2-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="9e6b2-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e6b2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e6b2-114">Remarks</span></span>

<span data-ttu-id="9e6b2-115">Эти свойства в набор символов 7-битовое сопоставить свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e6b2-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="9e6b2-116">Некоторые систем обмена сообщениями, такие как Интернет, а также некоторые ссылки X.400 не более 128-7-битовое ASCII кода кодировку.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="9e6b2-117">Производительность шлюзов для таких систем обмена сообщениями можно увеличить путем вызова метода [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) непосредственно для получения этого свойства, тем самым позволяет избежать дополнительной обработки для преобразования кода.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9e6b2-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e6b2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e6b2-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9e6b2-119">Protocol specifications</span></span>

<span data-ttu-id="9e6b2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e6b2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e6b2-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e6b2-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e6b2-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e6b2-123">Задает свойства и операции над списками пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="9e6b2-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e6b2-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e6b2-125">Обрабатывает клиентами с NSPI-сервера.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="9e6b2-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e6b2-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e6b2-127">Обрабатывает порядке и потоков данных, который используется для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="9e6b2-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e6b2-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e6b2-129">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9e6b2-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e6b2-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e6b2-131">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e6b2-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9e6b2-132">Header files</span></span>

<span data-ttu-id="9e6b2-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e6b2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9e6b2-134">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="9e6b2-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e6b2-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e6b2-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9e6b2-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e6b2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9e6b2-137">See also</span></span>



[<span data-ttu-id="9e6b2-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e6b2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e6b2-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e6b2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e6b2-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9e6b2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e6b2-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9e6b2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

