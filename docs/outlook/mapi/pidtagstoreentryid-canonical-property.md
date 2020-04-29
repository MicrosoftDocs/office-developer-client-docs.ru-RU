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
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278752"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="178b4-103">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="178b4-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="178b4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="178b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="178b4-105">Содержит уникальный идентификатор хранилища сообщений, в котором находится объект.</span><span class="sxs-lookup"><span data-stu-id="178b4-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="178b4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="178b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="178b4-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="178b4-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="178b4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="178b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="178b4-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="178b4-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="178b4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="178b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="178b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="178b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="178b4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="178b4-112">Area:</span></span>  <br/> |<span data-ttu-id="178b4-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="178b4-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="178b4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="178b4-114">Remarks</span></span>

<span data-ttu-id="178b4-115">Это свойство используется для открытия хранилища сообщений с помощью метода [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="178b4-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="178b4-116">Он также используется, чтобы открыть любой объект, принадлежащий хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="178b4-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="178b4-117">Для хранилища сообщений это свойство идентично свойству **PR_ENTRYID** собственного хранилища ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="178b4-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="178b4-118">Клиентское приложение может сравнить два свойства с помощью метода [IMAPISession:: метод compareentryids](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="178b4-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="178b4-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="178b4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="178b4-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="178b4-120">Protocol specifications</span></span>

<span data-ttu-id="178b4-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178b4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178b4-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="178b4-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="178b4-123">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178b4-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178b4-124">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="178b4-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="178b4-125">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178b4-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178b4-126">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="178b4-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="178b4-127">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178b4-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178b4-128">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="178b4-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="178b4-129">[[MS — ОКСШАРЕ]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178b4-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178b4-130">Предоставляет общий доступ к папкам почтового ящика между клиентами.</span><span class="sxs-lookup"><span data-stu-id="178b4-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="178b4-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="178b4-131">Header files</span></span>

<span data-ttu-id="178b4-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="178b4-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="178b4-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="178b4-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="178b4-134">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="178b4-134">Mapitags.h</span></span>
  
> <span data-ttu-id="178b4-135">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="178b4-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="178b4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="178b4-136">See also</span></span>



[<span data-ttu-id="178b4-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="178b4-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="178b4-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="178b4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="178b4-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="178b4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="178b4-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="178b4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

