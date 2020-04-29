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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415154"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="dae01-103">Каноническое свойство PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="dae01-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="dae01-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dae01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dae01-105">Содержит старый стиль (Microsoft Outlook 2002 и более ранние версии) идентификатора записи для хранилища сообщений Microsoft Exchange Server 2010 или Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dae01-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dae01-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dae01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dae01-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="dae01-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="dae01-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dae01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dae01-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="dae01-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="dae01-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dae01-110">Data type:</span></span>  <br/> |<span data-ttu-id="dae01-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dae01-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dae01-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dae01-112">Area:</span></span>  <br/> |<span data-ttu-id="dae01-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="dae01-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dae01-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="dae01-114">Remarks</span></span>

<span data-ttu-id="dae01-115">Начиная с Microsoft Outlook 2003, полные доменные имена сервера были интегрированы в идентификаторы записей, что позволяет избежать дополнительных вызовов RPC для ссылок.</span><span class="sxs-lookup"><span data-stu-id="dae01-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="dae01-116">Тем не менее, это делает идентификаторы записей более длинными и вводит дополнительные сценарии, в которых метод **метод compareentryids** должен использоваться для определения того, эквивалентны ли два идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="dae01-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="dae01-117">Свойство PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) получает доступ к старому формату идентификатора записи Exchange Server, используемого Microsoft Outlook 2002 (Microsoft Office XP) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="dae01-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="dae01-118">Это может сэкономить место, а также сократить количество вызовов **метод compareentryids** , необходимых для определения того, когда идентификаторы записей эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="dae01-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="dae01-119">Обратите внимание на то, что использование старых идентификаторов записей для открытия почтового ящика может привести к дополнительным RPC, если требуется ссылка.</span><span class="sxs-lookup"><span data-stu-id="dae01-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="dae01-120">Чтобы получить доступ к свойству PR_STORE_ENTRYID_EMSMDB_V1 в режиме кэширования, необходимо обойти кэш, используя флаг MAPI_NO_CACHE с методом [IMAPIProp::/PROPS](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dae01-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="dae01-121">Если **PR_STORE_ENTRYID_EMSMDB_V1** недоступен, код должен вернуться в PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="dae01-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="dae01-122">Свойство PR_STORE_ENTRYID_EMSMDB_V1 поддерживает только Outlook 2003 с помощью Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="dae01-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dae01-123">См. также</span><span class="sxs-lookup"><span data-stu-id="dae01-123">See also</span></span>



[<span data-ttu-id="dae01-124">Каноническое свойство PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="dae01-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="dae01-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dae01-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dae01-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="dae01-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dae01-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dae01-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dae01-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dae01-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

