---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427089"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="4ce35-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="4ce35-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="4ce35-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ce35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ce35-105">Позволяет поставщику хранения сообщений выполнять обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ce35-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="4ce35-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ce35-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="4ce35-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4ce35-107">Parameters</span></span>

 <span data-ttu-id="4ce35-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ce35-108">_ulFlags_</span></span>
  
> <span data-ttu-id="4ce35-109">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="4ce35-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4ce35-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ce35-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="4ce35-111">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4ce35-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4ce35-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ce35-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="4ce35-113">[in] Указатель на идентификатор записи обрабатываемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ce35-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ce35-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ce35-114">Return value</span></span>

<span data-ttu-id="4ce35-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ce35-115">S_OK</span></span> 
  
> <span data-ttu-id="4ce35-116">Обработка отправленного сообщения прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="4ce35-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="4ce35-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4ce35-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4ce35-118">Поставщик магазина сообщений не поддерживает обработку отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4ce35-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="4ce35-119">Это значение ошибки возвращается, если вызываемая не является шпалером MAPI.</span><span class="sxs-lookup"><span data-stu-id="4ce35-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ce35-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ce35-120">Remarks</span></span>

<span data-ttu-id="4ce35-121">Метод **IMsgStore::FinishedMsg** выполняет обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ce35-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="4ce35-122">Эта обработка может включать удаление сообщения, перемещение его в другую папку или оба действия.</span><span class="sxs-lookup"><span data-stu-id="4ce35-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="4ce35-123">Тип обработки зависит от **того,** заданы ли свойства [PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)и **PR_SENTMAIL_ENTRYID** [(PidTagSentMailEntryId).](pidtagsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4ce35-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4ce35-124">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4ce35-124">Notes to implementers</span></span>

<span data-ttu-id="4ce35-125">В реализации **FinishedMsg** разблокировать сообщение, идентифицированное  _lpEntryID,_ и выполнить соответствующую обработку.</span><span class="sxs-lookup"><span data-stu-id="4ce35-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="4ce35-126">Целевое сообщение всегда будет заблокировано; spooler MAPI никогда не передает идентификатор записи для разблокированного сообщения **в FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="4ce35-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="4ce35-127">Не исключено,  что PR_DELETE_AFTER_SUBMIT **или PR_SENTMAIL_ENTRYID** не за установлено, либо установлено одно или другое.</span><span class="sxs-lookup"><span data-stu-id="4ce35-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="4ce35-128">В следующей таблице описывается действие, необходимое для параметров:</span><span class="sxs-lookup"><span data-stu-id="4ce35-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ce35-129">Если не установлено ни одно свойство:</span><span class="sxs-lookup"><span data-stu-id="4ce35-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="4ce35-130">Оставьте сообщение в папке, из которой оно было отправлено (как правило, в папке Outbox).</span><span class="sxs-lookup"><span data-stu-id="4ce35-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="4ce35-131">Если за набором обоих свойств:</span><span class="sxs-lookup"><span data-stu-id="4ce35-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="4ce35-132">При желании переместим сообщение в указанную папку и удалите его.</span><span class="sxs-lookup"><span data-stu-id="4ce35-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="4ce35-133">Если PR_SENTMAIL_ENTRYID установлено:</span><span class="sxs-lookup"><span data-stu-id="4ce35-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="4ce35-134">Перемещение сообщения в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="4ce35-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="4ce35-135">Если PR_DELETE_AFTER_SUBMIT установлено:</span><span class="sxs-lookup"><span data-stu-id="4ce35-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="4ce35-136">Удаление сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ce35-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="4ce35-137">После принятия необходимых действий позвоните в [метод IMAPISupport::D OSentMail.](imapisupport-dosentmail.md)</span><span class="sxs-lookup"><span data-stu-id="4ce35-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ce35-138">См. также</span><span class="sxs-lookup"><span data-stu-id="4ce35-138">See also</span></span>



[<span data-ttu-id="4ce35-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="4ce35-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="4ce35-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4ce35-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

