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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278773"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="58093-103">Каноническое свойство PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="58093-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="58093-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58093-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58093-105">Содержит старый стиль (Microsoft Outlook 2002 и более ранние версии) идентификатора записи для хранилища сообщений Microsoft Exchange Server 2010 или Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58093-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58093-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="58093-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58093-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="58093-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="58093-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="58093-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58093-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="58093-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="58093-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="58093-110">Data type:</span></span>  <br/> |<span data-ttu-id="58093-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="58093-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="58093-112">Область:</span><span class="sxs-lookup"><span data-stu-id="58093-112">Area:</span></span>  <br/> |<span data-ttu-id="58093-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="58093-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58093-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="58093-114">Remarks</span></span>

<span data-ttu-id="58093-115">Начиная с Microsoft Outlook 2003, полные доменные имена сервера были интегрированы в идентификаторы записей, что позволяет избежать дополнительных вызовов RPC для ссылок.</span><span class="sxs-lookup"><span data-stu-id="58093-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="58093-116">Тем не менее, это делает идентификаторы записей более длинными и вводит дополнительные сценарии, в которых метод **метод compareentryids** должен использоваться для определения того, эквивалентны ли два идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="58093-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="58093-117">Свойство PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) получает доступ к старому формату идентификатора записи Exchange Server, используемого Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="58093-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="58093-118">Это может сэкономить место, а также сократить количество вызовов **метод compareentryids** , необходимых для определения того, когда идентификаторы записей эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="58093-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="58093-119">Обратите внимание на то, что использование старых идентификаторов записей для открытия почтового ящика может привести к дополнительным RPC, если требуется ссылка.</span><span class="sxs-lookup"><span data-stu-id="58093-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="58093-120">Чтобы получить доступ к свойству PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования, необходимо обойти кэш с помощью флага МАПИ_НО_КАЧЕ с методом [IMAPIProp::](imapiprop-getprops.md) GetProperty.</span><span class="sxs-lookup"><span data-stu-id="58093-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="58093-121">Если **PR_STORE_ENTRYID_EMSMDB_V1** недоступен, код должен ВОЗВРАЩАТЬСЯ к пр_сторе_ентрид.</span><span class="sxs-lookup"><span data-stu-id="58093-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="58093-122">Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживается только для Outlook 2003 с помощью Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="58093-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58093-123">См. также</span><span class="sxs-lookup"><span data-stu-id="58093-123">See also</span></span>



[<span data-ttu-id="58093-124">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="58093-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="58093-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="58093-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58093-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="58093-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58093-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="58093-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58093-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="58093-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

