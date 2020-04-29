---
title: имсгсторежетаутгоингкуеуе
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
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434153"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="d791b-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="d791b-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="d791b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d791b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d791b-105">Предоставляет доступ к таблице исходящей очереди, таблице, содержащей сведения обо всех сообщениях в исходящей очереди хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d791b-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="d791b-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="d791b-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d791b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d791b-107">Parameters</span></span>

 <span data-ttu-id="d791b-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d791b-108">_ulFlags_</span></span>
  
> <span data-ttu-id="d791b-109">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d791b-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d791b-110">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="d791b-110">_lppTable_</span></span>
  
> <span data-ttu-id="d791b-111">вышли Указатель на указатель на таблицу "очередь исходящих сообщений".</span><span class="sxs-lookup"><span data-stu-id="d791b-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d791b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d791b-112">Return value</span></span>

<span data-ttu-id="d791b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d791b-113">S_OK</span></span> 
  
> <span data-ttu-id="d791b-114">Таблица исходящих сообщений успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="d791b-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d791b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d791b-115">Remarks</span></span>

<span data-ttu-id="d791b-116">Метод **IMsgStore:: жетаутгоингкуеуе** предоставляет диспетчер очереди MAPI с доступом к таблице, в которой отображается очередь исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d791b-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="d791b-117">Как правило, сообщения помещаются в таблицу исходящих очередей после вызова метода [iMessage:: субмитмессаже](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d791b-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="d791b-118">Тем не менее, так как порядок отправки влияет на порядок предварительной обработки и отправки поставщику транспорта, некоторые сообщения, помеченные для отправки, могут не отображаться в таблице очереди исходящих сообщений сразу же.</span><span class="sxs-lookup"><span data-stu-id="d791b-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d791b-119">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d791b-119">Notes to implementers</span></span>

<span data-ttu-id="d791b-120">Список свойств, которые необходимо включить в качестве столбцов в таблице исходящей очереди, можно найти в статье [очередь исходящих](outgoing-queue-tables.md)сообщений.</span><span class="sxs-lookup"><span data-stu-id="d791b-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="d791b-121">Так как диспетчер очереди MAPI предназначен для приема сообщений из хранилища сообщений в порядке возрастания времени отправки, можно разрешить диспетчеру очереди MAPI сортировать таблицу исходящей очереди в соответствии с этим заказом или задать его в качестве порядка сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d791b-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="d791b-122">Необходимо поддерживать уведомления для таблицы исходящих сообщений "очередь сообщений", гарантируя, что диспетчер очереди MAPI уведомляется при изменении содержимого очереди.</span><span class="sxs-lookup"><span data-stu-id="d791b-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d791b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d791b-123">See also</span></span>



[<span data-ttu-id="d791b-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d791b-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="d791b-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d791b-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

