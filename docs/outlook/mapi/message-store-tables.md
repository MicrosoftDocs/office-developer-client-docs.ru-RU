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
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405354"
---
# <a name="message-store-tables"></a><span data-ttu-id="df834-103">Таблицы хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="df834-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="df834-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df834-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df834-105">Таблица "хранилище сообщений" содержит сведения о поставщиках хранилища сообщений в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="df834-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="df834-106">Для каждого сеанса MAPI существует одна таблица хранилища сообщений, реализованная MAPI и используемая клиентами.</span><span class="sxs-lookup"><span data-stu-id="df834-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="df834-107">Клиенты могут использовать эту таблицу, например, для обнаружения всех экземпляров определенного поставщика или для обнаружения определенного хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="df834-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="df834-108">Таблица хранилища сообщений является динамической.</span><span class="sxs-lookup"><span data-stu-id="df834-108">The message store table is dynamic.</span></span> <span data-ttu-id="df834-109">Если пользователь клиентского приложения изменяет профиль, изменяя хранилище сообщений по умолчанию, например, значения свойств **пр_дефаулт_сторе** для соответствующих хранилищ сообщений немедленно обновляются.</span><span class="sxs-lookup"><span data-stu-id="df834-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="df834-110">Клиенты обращаются к таблице хранилища сообщений, вызывая метод [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="df834-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="df834-111">Следующие свойства составляют обязательный набор столбцов в таблице хранилища сообщений:</span><span class="sxs-lookup"><span data-stu-id="df834-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df834-112">**Пр_дефаулт_сторе** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df834-113">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df834-114">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df834-115">**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df834-116">**Пр_мдб_провидер** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df834-117">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df834-118">**Пр_провидер_дисплай** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df834-119">**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="df834-120">**Пр_ресаурце_флагс** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="df834-121">**Пр_ресаурце_типе** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="df834-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df834-122">См. также</span><span class="sxs-lookup"><span data-stu-id="df834-122">See also</span></span>



[<span data-ttu-id="df834-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="df834-123">MAPI Tables</span></span>](mapi-tables.md)

