---
title: Каноническое свойство PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d6f858a9f1d3d4620a86621e3f5ecb4ad4609691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278732"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="cc428-103">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="cc428-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="cc428-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc428-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc428-105">Содержит уникальный двоичный код (ключ записи) хранилища сообщений, в котором находится объект.</span><span class="sxs-lookup"><span data-stu-id="cc428-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc428-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cc428-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc428-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="cc428-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="cc428-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cc428-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc428-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="cc428-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="cc428-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cc428-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc428-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc428-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc428-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cc428-112">Area:</span></span>  <br/> |<span data-ttu-id="cc428-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="cc428-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc428-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc428-114">Remarks</span></span>

<span data-ttu-id="cc428-115">Для хранилища сообщений это свойство идентично свойству **PR_RECORD_KEY** собственного хранилища ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc428-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="cc428-116">Отношение между этим свойством и **PR_RECORD_KEY** это то же, что и отношение между **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc428-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc428-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc428-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc428-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cc428-118">Protocol specifications</span></span>

<span data-ttu-id="cc428-119">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc428-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc428-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="cc428-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cc428-121">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc428-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc428-122">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="cc428-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc428-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cc428-123">Header files</span></span>

<span data-ttu-id="cc428-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cc428-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc428-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cc428-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc428-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="cc428-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cc428-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="cc428-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc428-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cc428-128">See also</span></span>



[<span data-ttu-id="cc428-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cc428-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc428-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="cc428-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc428-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cc428-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc428-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cc428-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

