---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809386"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="15844-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="15844-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="15844-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15844-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15844-105">Предоставляет доступ к таблице исходящей очереди, таблицы, которая содержит сведения обо всех сообщений в очереди исходящих хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="15844-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="15844-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="15844-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="15844-107">���������</span><span class="sxs-lookup"><span data-stu-id="15844-107">Parameters</span></span>

 <span data-ttu-id="15844-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15844-108">_ulFlags_</span></span>
  
> <span data-ttu-id="15844-109">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="15844-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="15844-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="15844-110">_lppTable_</span></span>
  
> <span data-ttu-id="15844-111">[out] Указатель на указатель на таблице исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="15844-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15844-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="15844-112">Return value</span></span>

<span data-ttu-id="15844-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="15844-113">S_OK</span></span> 
  
> <span data-ttu-id="15844-114">В таблице исходящей очереди успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="15844-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15844-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="15844-115">Remarks</span></span>

<span data-ttu-id="15844-116">Метод **IMsgStore::GetOutgoingQueue** предоставляет диспетчер очереди MAPI с доступом к таблица, показывающая хранилища сообщений очереди исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="15844-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="15844-117">Как правило сообщения помещаются в таблицу исходящей очереди после вызова метода их [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="15844-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="15844-118">Тем не менее так как порядок отправки влияет на порядок обработки и отправки для поставщика транспорта, некоторые сообщения, помеченные для отправки могут не отображаться в таблице исходящей очереди немедленно.</span><span class="sxs-lookup"><span data-stu-id="15844-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="15844-119">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="15844-119">Notes to implementers</span></span>

<span data-ttu-id="15844-120">Чтобы получить список свойств, которые должны быть включены в качестве столбцов в таблице исходящей очереди см [исходящей очереди](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="15844-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="15844-121">Поскольку диспетчер очереди MAPI разработан для приема сообщений из хранилища сообщений по возрастанию время отправки, либо разрешить диспетчер очереди MAPI для сортировки исходящей очереди в соответствии с этой порядке или установить как порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15844-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="15844-122">Должен поддерживать уведомления для в таблице очереди исходящих сообщений проверка того, что диспетчер очереди MAPI получает уведомление при изменении содержимого очереди.</span><span class="sxs-lookup"><span data-stu-id="15844-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15844-123">См. также</span><span class="sxs-lookup"><span data-stu-id="15844-123">See also</span></span>



[<span data-ttu-id="15844-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="15844-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="15844-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="15844-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

