---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d06523625a20760faec7a6c73a6beaef757818b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575079"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="73b2e-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="73b2e-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="73b2e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73b2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73b2e-105">Задание состояния, связанный с сообщением (например, будет ли это сообщение помечено для удаления).</span><span class="sxs-lookup"><span data-stu-id="73b2e-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="73b2e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73b2e-106">Parameters</span></span>

 <span data-ttu-id="73b2e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="73b2e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="73b2e-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="73b2e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="73b2e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="73b2e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="73b2e-110">[in] Указатель на идентификатор записи для сообщения, состояние которого имеет значение.</span><span class="sxs-lookup"><span data-stu-id="73b2e-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="73b2e-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="73b2e-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="73b2e-112">[in] Новое состояние для назначения.</span><span class="sxs-lookup"><span data-stu-id="73b2e-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="73b2e-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="73b2e-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="73b2e-114">[in] Битовая маска флаги, которая применяется к новое состояние и указывает флаги должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="73b2e-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="73b2e-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="73b2e-115">The following flags can be set:</span></span>
    
<span data-ttu-id="73b2e-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="73b2e-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="73b2e-117">Сообщение было помечено для удаления.</span><span class="sxs-lookup"><span data-stu-id="73b2e-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="73b2e-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="73b2e-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="73b2e-119">Сообщение является не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="73b2e-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="73b2e-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="73b2e-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="73b2e-121">Это сообщение будет отображаться выделенный.</span><span class="sxs-lookup"><span data-stu-id="73b2e-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="73b2e-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="73b2e-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="73b2e-123">Сообщение было помечено для удаления в магазине удаленных сообщений без загрузки локального клиента.</span><span class="sxs-lookup"><span data-stu-id="73b2e-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="73b2e-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="73b2e-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="73b2e-125">Сообщение было помечено для загрузки с хранения удаленных сообщений для локального клиента.</span><span class="sxs-lookup"><span data-stu-id="73b2e-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="73b2e-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="73b2e-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="73b2e-127">Сообщение уже помечен для определенного клиента цели.</span><span class="sxs-lookup"><span data-stu-id="73b2e-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="73b2e-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="73b2e-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="73b2e-129">[out] Указатель на предыдущем состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="73b2e-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73b2e-130">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="73b2e-130">Return value</span></span>

<span data-ttu-id="73b2e-131">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="73b2e-131">S_OK</span></span> 
  
> <span data-ttu-id="73b2e-132">Сообщение было успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="73b2e-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73b2e-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="73b2e-133">Remarks</span></span>

<span data-ttu-id="73b2e-134">Метод **IMAPIFolder::SetMessageStatus** задает состояние сообщения значения, которые хранятся в своем свойстве **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="73b2e-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73b2e-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="73b2e-135">Notes to implementers</span></span>

<span data-ttu-id="73b2e-136">Как задать, снят и используется биты состояния сообщение полностью зависит от реализации, за исключением того, что бит 0 до 15 зарезервированы и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="73b2e-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="73b2e-137">Реализация поставщика транспорта удаленного этого метода должны соответствовать описанной здесь семантики.</span><span class="sxs-lookup"><span data-stu-id="73b2e-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="73b2e-138">Существует не особенности.</span><span class="sxs-lookup"><span data-stu-id="73b2e-138">There are no special considerations.</span></span> <span data-ttu-id="73b2e-139">Клиенты используют этот метод для установки битов MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE означает, что конкретное сообщение для загрузки или удалены из хранилища удаленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="73b2e-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="73b2e-140">Поставщик удаленного транспорта не требуется реализовать метод [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) связанных с ними.</span><span class="sxs-lookup"><span data-stu-id="73b2e-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="73b2e-141">Клиенты должны выглядеть в таблице содержимое папки для определения статуса сообщения.</span><span class="sxs-lookup"><span data-stu-id="73b2e-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="73b2e-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="73b2e-142">Notes to callers</span></span>

<span data-ttu-id="73b2e-143">Свойство **PR_MSG_STATUS** сообщения можно использовать для согласования режим блокировки сообщений с помощью других клиентов.</span><span class="sxs-lookup"><span data-stu-id="73b2e-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="73b2e-144">Назначить немного как флаг блокировки.</span><span class="sxs-lookup"><span data-stu-id="73b2e-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="73b2e-145">Чтобы определить, было ли задано разрядная блокировки, проверьте предыдущее состояние сообщения с помощью параметра _lpulOldStatus_ .</span><span class="sxs-lookup"><span data-stu-id="73b2e-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="73b2e-146">Используйте другие двоичных файлов с помощью параметра _ulNewStatus_ для отслеживания состояния сообщения не мешая разрядная блокировки.</span><span class="sxs-lookup"><span data-stu-id="73b2e-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73b2e-147">См. также</span><span class="sxs-lookup"><span data-stu-id="73b2e-147">See also</span></span>



[<span data-ttu-id="73b2e-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="73b2e-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="73b2e-149">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="73b2e-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="73b2e-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="73b2e-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

