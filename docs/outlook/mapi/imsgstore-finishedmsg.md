---
title: Имсгсторефинишедмсг
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348764"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="9366e-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="9366e-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="9366e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9366e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9366e-105">Позволяет поставщику хранилища сообщений выполнять обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9366e-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="9366e-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="9366e-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="9366e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9366e-107">Parameters</span></span>

 <span data-ttu-id="9366e-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9366e-108">_ulFlags_</span></span>
  
> <span data-ttu-id="9366e-109">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="9366e-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9366e-110">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="9366e-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="9366e-111">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="9366e-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9366e-112">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="9366e-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="9366e-113">возврата Указатель на идентификатор записи обрабатываемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9366e-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9366e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9366e-114">Return value</span></span>

<span data-ttu-id="9366e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9366e-115">S_OK</span></span> 
  
> <span data-ttu-id="9366e-116">Обработка отправленного сообщения выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9366e-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="9366e-117">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="9366e-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9366e-118">Поставщик хранилища сообщений не поддерживает отправную обработку сообщений.</span><span class="sxs-lookup"><span data-stu-id="9366e-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="9366e-119">Это значение ошибки возвращается, если вызывающий абонент не является диспетчером MAPI.</span><span class="sxs-lookup"><span data-stu-id="9366e-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9366e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="9366e-120">Remarks</span></span>

<span data-ttu-id="9366e-121">Метод **IMsgStore:: финишедмсг** выполняет обработку отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9366e-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="9366e-122">Эта обработка может привести к удалению сообщения, перемещению его в другую папку или обоим действиям.</span><span class="sxs-lookup"><span data-stu-id="9366e-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="9366e-123">Тип обработки зависит от того, заданы ли свойства **пр_делете_афтер_субмит** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) и **пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9366e-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9366e-124">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9366e-124">Notes to implementers</span></span>

<span data-ttu-id="9366e-125">В реализации **финишедмсг**Разблокируйте сообщение, определяемое _лпентрид_ , и выполните соответствующую обработку.</span><span class="sxs-lookup"><span data-stu-id="9366e-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="9366e-126">Конечное сообщение всегда будет заблокировано; Диспетчер очереди MAPI никогда не передает идентификатор записи для незаблокированного сообщения в **финишедмсг**.</span><span class="sxs-lookup"><span data-stu-id="9366e-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="9366e-127">Возможно, не задано ни **пр_делете_афтер_субмит** , ни **пр_сентмаил_ентрид** , задано значение, либо задано значение One или other.</span><span class="sxs-lookup"><span data-stu-id="9366e-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="9366e-128">В следующей таблице описаны действия, которые необходимо выполнить в соответствии с параметрами:</span><span class="sxs-lookup"><span data-stu-id="9366e-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9366e-129">Если не задано ни одно свойство:</span><span class="sxs-lookup"><span data-stu-id="9366e-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="9366e-130">Оставьте сообщение в папке, из которой оно было отправлено (обычно это папка "исХодящая").</span><span class="sxs-lookup"><span data-stu-id="9366e-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="9366e-131">Если заданы оба свойства:</span><span class="sxs-lookup"><span data-stu-id="9366e-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="9366e-132">При необходимости переместите сообщение в указанную папку, а затем удалите его.</span><span class="sxs-lookup"><span data-stu-id="9366e-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="9366e-133">Если задано значение ПР_СЕНТМАИЛ_ЕНТРИД:</span><span class="sxs-lookup"><span data-stu-id="9366e-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="9366e-134">Переместить сообщение в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="9366e-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="9366e-135">Если задано значение ПР_ДЕЛЕТЕ_АФТЕР_СУБМИТ:</span><span class="sxs-lookup"><span data-stu-id="9366e-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="9366e-136">Удаление сообщения.</span><span class="sxs-lookup"><span data-stu-id="9366e-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="9366e-137">ВыПолнив все необходимые действия, вызовите метод [имаписуппорт::D осентмаил](imapisupport-dosentmail.md) .</span><span class="sxs-lookup"><span data-stu-id="9366e-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9366e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9366e-138">See also</span></span>



[<span data-ttu-id="9366e-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="9366e-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="9366e-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9366e-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

