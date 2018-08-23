---
title: Каноническое свойство PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 02d2c30fede7e554910a1bedb01b79c488447bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595358"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="b40d7-103">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="b40d7-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="b40d7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b40d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b40d7-105">Содержит заданный поставщиком [MAPIUID](mapiuid.md) структуру, указывающую тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b40d7-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b40d7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b40d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b40d7-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="b40d7-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="b40d7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b40d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b40d7-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="b40d7-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="b40d7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b40d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="b40d7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b40d7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b40d7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b40d7-112">Area:</span></span>  <br/> |<span data-ttu-id="b40d7-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="b40d7-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b40d7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b40d7-114">Remarks</span></span>

<span data-ttu-id="b40d7-115">Структура [MAPIUID](mapiuid.md) определяет тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b40d7-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="b40d7-116">Значение вычисляется поставщиками хранилища сообщений на объектов хранилища сообщений и является уникальным для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="b40d7-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="b40d7-117">Он обычно используется при просмотре в таблице хранилища сообщений для поиска хранилище требуемого типа, таких как общие папки.</span><span class="sxs-lookup"><span data-stu-id="b40d7-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="b40d7-118">Это свойство является аналогом свойство **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) для адресных книг.</span><span class="sxs-lookup"><span data-stu-id="b40d7-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b40d7-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b40d7-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b40d7-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b40d7-120">Header files</span></span>

<span data-ttu-id="b40d7-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b40d7-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b40d7-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b40d7-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b40d7-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b40d7-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b40d7-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b40d7-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b40d7-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b40d7-125">See also</span></span>



[<span data-ttu-id="b40d7-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b40d7-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b40d7-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b40d7-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b40d7-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b40d7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b40d7-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b40d7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

