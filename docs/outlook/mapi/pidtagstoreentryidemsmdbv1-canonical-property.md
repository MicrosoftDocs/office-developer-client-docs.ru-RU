---
title: Каноническое свойство PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 505ea9ba5d7105f20f335035e42286fdab1cb1aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576325"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="9535a-103">Каноническое свойство PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="9535a-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="9535a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9535a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9535a-105">Содержит старый стиль (Microsoft Outlook 2002 и более ранних версий) идентификатор записи банка сообщений Microsoft Exchange Server 2010 или Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9535a-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9535a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9535a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9535a-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="9535a-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="9535a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9535a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9535a-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="9535a-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="9535a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9535a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9535a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9535a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9535a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9535a-112">Area:</span></span>  <br/> |<span data-ttu-id="9535a-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="9535a-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9535a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9535a-114">Remarks</span></span>

<span data-ttu-id="9535a-115">Начиная с Microsoft Outlook 2003, полные доменные имена серверов были интегрированы в идентификаторы, тем самым позволяет избежать дополнительных RPC для ссылок.</span><span class="sxs-lookup"><span data-stu-id="9535a-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="9535a-116">Тем не менее это делает запись идентификаторы больше времени и приводятся ссылки на дополнительные сценарии использования метода **CompareEntryIDs** для определения ли два запись идентификаторы эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="9535a-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="9535a-117">PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) свойство обращается к старый формат идентификатор записи Exchange Server, используемый с Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="9535a-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="9535a-118">Это можно сохранить пространство и также сократить количество вызовов **CompareEntryIDs** , необходимо определить, когда запись идентификаторы эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="9535a-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="9535a-119">Обратите внимание, что с помощью более старые записи идентификаторов для открытия почтового ящика, могут вызвать некоторые дополнительные RPC Если ссылка является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9535a-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="9535a-120">Для доступа к свойству PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования данных, необходимо обойти кэша, используя флаг MAPI_NO_CACHE с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9535a-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="9535a-121">Если **PR_STORE_ENTRYID_EMSMDB_V1** недоступен, код должен вернуться к PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="9535a-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="9535a-122">Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживается только в Outlook 2003 через Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9535a-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9535a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9535a-123">See also</span></span>



[<span data-ttu-id="9535a-124">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="9535a-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="9535a-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9535a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9535a-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9535a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9535a-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9535a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9535a-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9535a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

