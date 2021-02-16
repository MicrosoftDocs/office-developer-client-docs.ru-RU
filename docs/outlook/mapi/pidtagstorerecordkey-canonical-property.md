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
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="874e3-103">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="874e3-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="874e3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="874e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="874e3-105">Содержит уникальный двоичный сравнимый идентификатор (ключ записи) в хранилище сообщений, в котором находится объект.</span><span class="sxs-lookup"><span data-stu-id="874e3-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="874e3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="874e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="874e3-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="874e3-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="874e3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="874e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="874e3-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="874e3-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="874e3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="874e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="874e3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="874e3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="874e3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="874e3-112">Area:</span></span>  <br/> |<span data-ttu-id="874e3-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="874e3-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="874e3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="874e3-114">Remarks</span></span>

<span data-ttu-id="874e3-115">Для хранения сообщений это свойство идентично свойству PR_RECORD_KEY[(PidTagRecordKey).](pidtagrecordkey-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="874e3-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="874e3-116">Отношения между этим свойством **и** PR_RECORD_KEY такие же, как и отношения между **PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)и **PR_ENTRYID** ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="874e3-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="874e3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="874e3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="874e3-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="874e3-118">Protocol specifications</span></span>

<span data-ttu-id="874e3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="874e3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="874e3-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="874e3-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="874e3-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="874e3-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="874e3-122">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="874e3-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="874e3-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="874e3-123">Header files</span></span>

<span data-ttu-id="874e3-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="874e3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="874e3-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="874e3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="874e3-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="874e3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="874e3-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="874e3-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="874e3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="874e3-128">See also</span></span>



[<span data-ttu-id="874e3-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="874e3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="874e3-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="874e3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="874e3-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="874e3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="874e3-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="874e3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

