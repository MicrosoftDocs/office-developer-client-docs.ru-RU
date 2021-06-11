---
title: Каноническое свойство PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422245"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="bb193-103">Каноническое свойство PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="bb193-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="bb193-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb193-105">Содержит структуру [MAPIUID поставщика адресных книг.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="bb193-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb193-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bb193-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb193-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="bb193-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="bb193-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bb193-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb193-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="bb193-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="bb193-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bb193-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb193-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb193-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb193-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bb193-112">Area:</span></span>  <br/> |<span data-ttu-id="bb193-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="bb193-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb193-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb193-114">Remarks</span></span>

<span data-ttu-id="bb193-115">Структура **MAPIUID** определяет, какой поставщик адресных книг поставляет этот контейнер в иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="bb193-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="bb193-116">Значение уникально для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="bb193-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="bb193-117">Поставщик адресных книг может предоставить несколько идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="bb193-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="bb193-118">Например, поставщик, который поставляет два разных контейнера, может публиковать в PR_AB_PROVIDER_ID **уникальные** идентификаторы для каждого контейнера.</span><span class="sxs-lookup"><span data-stu-id="bb193-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="bb193-119">**PR_AB_PROVIDER_ID** аналогично свойству **PR_MDB_PROVIDER** [(PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)для магазинов сообщений.</span><span class="sxs-lookup"><span data-stu-id="bb193-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="bb193-120">Клиентские приложения могут использовать **PR_AB_PROVIDER_ID** для поиска связанных строк в таблице иерархии адресных книг.</span><span class="sxs-lookup"><span data-stu-id="bb193-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb193-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bb193-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bb193-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="bb193-122">Header files</span></span>

<span data-ttu-id="bb193-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb193-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bb193-124">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="bb193-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="bb193-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb193-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb193-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bb193-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb193-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bb193-127">See also</span></span>



[<span data-ttu-id="bb193-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="bb193-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="bb193-129">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="bb193-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="bb193-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bb193-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb193-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bb193-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb193-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="bb193-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

