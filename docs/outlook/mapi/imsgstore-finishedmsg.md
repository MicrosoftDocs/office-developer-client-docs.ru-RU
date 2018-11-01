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
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589954"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="197cd-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="197cd-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="197cd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="197cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="197cd-105">Включает поставщика хранилища сообщений для обработки на отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="197cd-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="197cd-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="197cd-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="197cd-107">���������</span><span class="sxs-lookup"><span data-stu-id="197cd-107">Parameters</span></span>

 <span data-ttu-id="197cd-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="197cd-108">_ulFlags_</span></span>
  
> <span data-ttu-id="197cd-109">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="197cd-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="197cd-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="197cd-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="197cd-111">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="197cd-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="197cd-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="197cd-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="197cd-113">[in] Указатель на идентификатор записи сообщения для обработки.</span><span class="sxs-lookup"><span data-stu-id="197cd-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="197cd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="197cd-114">Return value</span></span>

<span data-ttu-id="197cd-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="197cd-115">S_OK</span></span> 
  
> <span data-ttu-id="197cd-116">Обработка в сообщении прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="197cd-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="197cd-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="197cd-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="197cd-118">Поставщик хранения сообщения не поддерживает обработки отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="197cd-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="197cd-119">Это значение ошибка возвращается в том случае, если вызывающий объект не является диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="197cd-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="197cd-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="197cd-120">Remarks</span></span>

<span data-ttu-id="197cd-121">Метод **IMsgStore::FinishedMsg** выполняет обработку отправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="197cd-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="197cd-122">В этом обработки может включать в себя удаление сообщений, перемещения в другую папку или оба действия.</span><span class="sxs-lookup"><span data-stu-id="197cd-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="197cd-123">Тип обработки зависит от того, является ли значение свойства **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) и **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="197cd-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="197cd-124">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="197cd-124">Notes to implementers</span></span>

<span data-ttu-id="197cd-125">В реализации **FinishedMsg**разблокировки сообщения, определяемую средством _lpEntryID_ и выполнить необходимые операции.</span><span class="sxs-lookup"><span data-stu-id="197cd-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="197cd-126">Сообщение целевой всегда будут удалены; Диспетчер очереди MAPI никогда не передает идентификатор записи для разблокированными сообщения **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="197cd-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="197cd-127">Существует возможность, что ни имеет значение **PR_DELETE_AFTER_SUBMIT** или **PR_SENTMAIL_ENTRYID** , как задать или задать одно или другое.</span><span class="sxs-lookup"><span data-stu-id="197cd-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="197cd-128">В следующей таблице описываются действия необходимо выполнить на основе параметров:</span><span class="sxs-lookup"><span data-stu-id="197cd-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="197cd-129">Если ни один из свойство имеет значение:</span><span class="sxs-lookup"><span data-stu-id="197cd-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="197cd-130">Оставьте сообщение в папку, из которого был отправлен (обычно исходящие).</span><span class="sxs-lookup"><span data-stu-id="197cd-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="197cd-131">Если заданы оба свойства:</span><span class="sxs-lookup"><span data-stu-id="197cd-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="197cd-132">Перемещение сообщения в указанной папки, если это необходимо и затем удалите его.</span><span class="sxs-lookup"><span data-stu-id="197cd-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="197cd-133">Если значение PR_SENTMAIL_ENTRYID:</span><span class="sxs-lookup"><span data-stu-id="197cd-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="197cd-134">Перемещение сообщения в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="197cd-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="197cd-135">Если значение PR_DELETE_AFTER_SUBMIT:</span><span class="sxs-lookup"><span data-stu-id="197cd-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="197cd-136">Удалите сообщение.</span><span class="sxs-lookup"><span data-stu-id="197cd-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="197cd-137">После выполнения действие соответствующие вызовите метод [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) .</span><span class="sxs-lookup"><span data-stu-id="197cd-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="197cd-138">См. также</span><span class="sxs-lookup"><span data-stu-id="197cd-138">See also</span></span>



[<span data-ttu-id="197cd-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="197cd-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="197cd-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="197cd-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

