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
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811968"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="85b05-103">Каноническое свойство PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="85b05-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="85b05-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85b05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85b05-105">Содержит старый стиль (Microsoft Outlook 2002 и более ранних версий) идентификатор записи банка сообщений Microsoft Exchange Server 2010 или Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85b05-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85b05-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="85b05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85b05-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="85b05-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="85b05-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="85b05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85b05-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="85b05-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="85b05-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="85b05-110">Data type:</span></span>  <br/> |<span data-ttu-id="85b05-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="85b05-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="85b05-112">Область:</span><span class="sxs-lookup"><span data-stu-id="85b05-112">Area:</span></span>  <br/> |<span data-ttu-id="85b05-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="85b05-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85b05-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="85b05-114">Remarks</span></span>

<span data-ttu-id="85b05-115">Начиная с Microsoft Outlook 2003, полные доменные имена серверов были интегрированы в идентификаторы, тем самым позволяет избежать дополнительных RPC для ссылок.</span><span class="sxs-lookup"><span data-stu-id="85b05-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="85b05-116">Тем не менее это делает запись идентификаторы больше времени и приводятся ссылки на дополнительные сценарии использования метода **CompareEntryIDs** для определения ли два запись идентификаторы эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="85b05-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="85b05-117">PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) свойство обращается к старый формат идентификатор записи Exchange Server, используемый с Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="85b05-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="85b05-118">Это можно сохранить пространство и также сократить количество вызовов **CompareEntryIDs** , необходимо определить, когда запись идентификаторы эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="85b05-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="85b05-119">Обратите внимание, что с помощью более старые записи идентификаторов для открытия почтового ящика, могут вызвать некоторые дополнительные RPC Если ссылка является обязательным.</span><span class="sxs-lookup"><span data-stu-id="85b05-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="85b05-120">Для доступа к свойству PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования данных, необходимо обойти кэша, используя флаг MAPI_NO_CACHE с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="85b05-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="85b05-121">Если **PR_STORE_ENTRYID_EMSMDB_V1** недоступен, код должен вернуться к PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="85b05-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="85b05-122">Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживается только в Outlook 2003 через Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="85b05-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85b05-123">См. также</span><span class="sxs-lookup"><span data-stu-id="85b05-123">See also</span></span>



[<span data-ttu-id="85b05-124">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="85b05-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="85b05-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="85b05-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85b05-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="85b05-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85b05-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="85b05-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85b05-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="85b05-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

