---
title: Таблицы магазина сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405354"
---
# <a name="message-store-tables"></a><span data-ttu-id="e1b19-103">Таблицы магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="e1b19-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="e1b19-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1b19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1b19-105">В таблице хранения сообщений содержатся сведения о поставщиках хранения сообщений в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="e1b19-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="e1b19-106">Существует одна таблица хранения сообщений для каждого сеанса MAPI, реализуемая MAPI и используемая клиентами.</span><span class="sxs-lookup"><span data-stu-id="e1b19-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="e1b19-107">Клиенты могут использовать эту таблицу, например, чтобы найти все экземпляры конкретного поставщика или найти определенный магазин сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1b19-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="e1b19-108">Таблица хранения сообщений динамическая.</span><span class="sxs-lookup"><span data-stu-id="e1b19-108">The message store table is dynamic.</span></span> <span data-ttu-id="e1b19-109">Если пользователь клиентского приложения изменяет профиль, например, изменяя хранилище сообщений  по умолчанию, значения свойств PR_DEFAULT_STORE для затронутых магазинов сообщений немедленно обновляются.</span><span class="sxs-lookup"><span data-stu-id="e1b19-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="e1b19-110">Клиенты получают доступ к таблице хранения сообщений, позвонив по [методу IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="e1b19-111">Следующие свойства составляют необходимый столбец, установленный в таблице хранения сообщений:</span><span class="sxs-lookup"><span data-stu-id="e1b19-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1b19-112">**PR_DEFAULT_STORE** [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e1b19-113">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e1b19-114">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e1b19-115">**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e1b19-116">**PR_MDB_PROVIDER** [(PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e1b19-117">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e1b19-118">**PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e1b19-119">**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1b19-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e1b19-120">**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e1b19-121">**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e1b19-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1b19-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e1b19-122">See also</span></span>



[<span data-ttu-id="e1b19-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="e1b19-123">MAPI Tables</span></span>](mapi-tables.md)

