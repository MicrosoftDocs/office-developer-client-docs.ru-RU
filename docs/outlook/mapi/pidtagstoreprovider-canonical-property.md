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
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811970"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="ac03b-103">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="ac03b-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="ac03b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac03b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac03b-105">Содержит заданный поставщиком [MAPIUID](mapiuid.md) структуру, указывающую тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ac03b-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac03b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ac03b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac03b-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="ac03b-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="ac03b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ac03b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac03b-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="ac03b-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="ac03b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ac03b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac03b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac03b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac03b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ac03b-112">Area:</span></span>  <br/> |<span data-ttu-id="ac03b-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="ac03b-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac03b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac03b-114">Remarks</span></span>

<span data-ttu-id="ac03b-115">Структура [MAPIUID](mapiuid.md) определяет тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ac03b-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="ac03b-116">Значение вычисляется поставщиками хранилища сообщений на объектов хранилища сообщений и является уникальным для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="ac03b-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="ac03b-117">Он обычно используется при просмотре в таблице хранилища сообщений для поиска хранилище требуемого типа, таких как общие папки.</span><span class="sxs-lookup"><span data-stu-id="ac03b-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="ac03b-118">Это свойство является аналогом свойство **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) для адресных книг.</span><span class="sxs-lookup"><span data-stu-id="ac03b-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac03b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac03b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac03b-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ac03b-120">Header files</span></span>

<span data-ttu-id="ac03b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac03b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac03b-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ac03b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac03b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac03b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ac03b-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ac03b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac03b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ac03b-125">See also</span></span>



[<span data-ttu-id="ac03b-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac03b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac03b-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac03b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac03b-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ac03b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac03b-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ac03b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

