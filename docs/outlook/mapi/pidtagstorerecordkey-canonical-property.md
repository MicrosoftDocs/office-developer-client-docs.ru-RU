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
ms.openlocfilehash: 4598ca5e654308f7701b1dd66adb227599773b7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811986"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="f653b-103">Каноническое свойство PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="f653b-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="f653b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f653b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f653b-105">Содержит уникальный идентификатор сравнимые двоичный файл (ключ записи) хранилища сообщений, в котором находится объект.</span><span class="sxs-lookup"><span data-stu-id="f653b-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f653b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f653b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f653b-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="f653b-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="f653b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f653b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f653b-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="f653b-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="f653b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f653b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f653b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f653b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f653b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f653b-112">Area:</span></span>  <br/> |<span data-ttu-id="f653b-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="f653b-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f653b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f653b-114">Remarks</span></span>

<span data-ttu-id="f653b-115">Для хранилища сообщений это свойство идентичен свойство магазина собственные **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f653b-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f653b-116">Отношения между это свойство и **PR_RECORD_KEY** -то же, что связь между **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f653b-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f653b-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f653b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f653b-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f653b-118">Protocol specifications</span></span>

<span data-ttu-id="f653b-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f653b-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f653b-120">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="f653b-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f653b-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f653b-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f653b-122">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="f653b-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f653b-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f653b-123">Header files</span></span>

<span data-ttu-id="f653b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f653b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f653b-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f653b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f653b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f653b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f653b-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f653b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f653b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f653b-128">See also</span></span>



[<span data-ttu-id="f653b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f653b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f653b-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f653b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f653b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f653b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f653b-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f653b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

