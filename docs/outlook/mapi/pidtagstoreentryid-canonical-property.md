---
title: Каноническое свойство PidTagStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ffe4798c5e8ef200619b060a58e868cc4a1b2bc2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590073"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="16d4a-103">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="16d4a-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="16d4a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16d4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16d4a-105">Содержит уникальный идентификатор хранилища сообщений, где находится объект.</span><span class="sxs-lookup"><span data-stu-id="16d4a-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16d4a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="16d4a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16d4a-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="16d4a-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="16d4a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="16d4a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16d4a-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="16d4a-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="16d4a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="16d4a-110">Data type:</span></span>  <br/> |<span data-ttu-id="16d4a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="16d4a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="16d4a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="16d4a-112">Area:</span></span>  <br/> |<span data-ttu-id="16d4a-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="16d4a-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16d4a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="16d4a-114">Remarks</span></span>

<span data-ttu-id="16d4a-115">Это свойство используется для открытия хранилища сообщений с помощью метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="16d4a-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="16d4a-116">Он также используется для открытия любой объект, владельцем которого является хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="16d4a-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="16d4a-117">Для хранилища сообщений это свойство идентичен свойство магазина собственные **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="16d4a-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="16d4a-118">Клиентское приложение позволяет сравнивать два свойства, с помощью метода [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="16d4a-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="16d4a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16d4a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16d4a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="16d4a-120">Protocol specifications</span></span>

<span data-ttu-id="16d4a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16d4a-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="16d4a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="16d4a-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4a-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16d4a-124">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="16d4a-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="16d4a-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4a-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16d4a-126">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="16d4a-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="16d4a-127">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4a-127">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16d4a-128">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="16d4a-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="16d4a-129">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4a-129">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16d4a-130">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="16d4a-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="16d4a-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="16d4a-131">Header files</span></span>

<span data-ttu-id="16d4a-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16d4a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="16d4a-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="16d4a-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="16d4a-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="16d4a-134">Mapitags.h</span></span>
  
> <span data-ttu-id="16d4a-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="16d4a-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16d4a-136">См. также</span><span class="sxs-lookup"><span data-stu-id="16d4a-136">See also</span></span>



[<span data-ttu-id="16d4a-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16d4a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16d4a-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16d4a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16d4a-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="16d4a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16d4a-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="16d4a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

