---
title: Таблицы хранилища сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810026"
---
# <a name="message-store-tables"></a><span data-ttu-id="33297-103">Таблицы хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="33297-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="33297-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33297-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33297-105">В таблице хранилища сообщений содержит сведения о поставщиках хранилища сообщений текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="33297-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="33297-106">Для каждого сеанса MAPI, реализованный MAPI и используемого клиентами имеется одна таблица хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="33297-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="33297-107">Клиенты могут использовать этой таблице, например, для поиска всех экземпляров определенного поставщика или найти конкретное сообщение хранилища.</span><span class="sxs-lookup"><span data-stu-id="33297-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="33297-108">В таблице хранилища сообщений динамических.</span><span class="sxs-lookup"><span data-stu-id="33297-108">The message store table is dynamic.</span></span> <span data-ttu-id="33297-109">Если пользователь клиентское приложение изменяет профиль, изменение хранилища сообщений по умолчанию, например, значения **PR_DEFAULT_STORE** свойства для хранилищ затронутых сообщения сразу же обновляются.</span><span class="sxs-lookup"><span data-stu-id="33297-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="33297-110">Для доступа клиентов к таблице хранилища сообщений путем вызова метода [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="33297-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="33297-111">Следующие свойства составляют обязательный столбец, задайте в таблице хранилища сообщений:</span><span class="sxs-lookup"><span data-stu-id="33297-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33297-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33297-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33297-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33297-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33297-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33297-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33297-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33297-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="33297-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="33297-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33297-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33297-122">См. также</span><span class="sxs-lookup"><span data-stu-id="33297-122">See also</span></span>



[<span data-ttu-id="33297-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="33297-123">MAPI Tables</span></span>](mapi-tables.md)

