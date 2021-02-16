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
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412053"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="63f54-103">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="63f54-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="63f54-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63f54-105">Содержит определяемую поставщиком [структуру MAPIUID,](mapiuid.md) которая указывает тип хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="63f54-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63f54-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="63f54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63f54-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="63f54-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="63f54-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="63f54-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63f54-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="63f54-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="63f54-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="63f54-110">Data type:</span></span>  <br/> |<span data-ttu-id="63f54-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="63f54-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="63f54-112">Область:</span><span class="sxs-lookup"><span data-stu-id="63f54-112">Area:</span></span>  <br/> |<span data-ttu-id="63f54-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="63f54-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63f54-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="63f54-114">Remarks</span></span>

<span data-ttu-id="63f54-115">Структура [MAPIUID](mapiuid.md) определяет тип хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="63f54-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="63f54-116">Значение вычисляется поставщиками хранилищей сообщений в объектах хранения сообщений и уникально для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="63f54-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="63f54-117">Обычно он используется для просмотра таблицы хранения сообщений, чтобы найти хранилище нужного типа, например общедоступные папки.</span><span class="sxs-lookup"><span data-stu-id="63f54-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="63f54-118">Это свойство аналогично свойству **PR_AB_PROVIDER_ID** ([PidTagAbProviderId)](pidtagabproviderid-canonical-property.md)для адресных книг.</span><span class="sxs-lookup"><span data-stu-id="63f54-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="63f54-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63f54-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="63f54-120">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="63f54-120">Header files</span></span>

<span data-ttu-id="63f54-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63f54-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="63f54-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="63f54-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="63f54-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63f54-123">Mapitags.h</span></span>
  
> <span data-ttu-id="63f54-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="63f54-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63f54-125">См. также</span><span class="sxs-lookup"><span data-stu-id="63f54-125">See also</span></span>



[<span data-ttu-id="63f54-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63f54-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63f54-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63f54-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63f54-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="63f54-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63f54-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="63f54-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

