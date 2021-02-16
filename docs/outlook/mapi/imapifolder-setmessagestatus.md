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
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417275"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="cc019-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="cc019-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="cc019-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc019-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc019-105">Задает состояние, связанное с сообщением (например, помечено ли это сообщение для удаления).</span><span class="sxs-lookup"><span data-stu-id="cc019-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="cc019-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc019-106">Parameters</span></span>

 <span data-ttu-id="cc019-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cc019-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="cc019-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="cc019-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cc019-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="cc019-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="cc019-110">[in] Указатель на идентификатор записи для сообщения, состояние которого установлено.</span><span class="sxs-lookup"><span data-stu-id="cc019-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="cc019-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="cc019-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="cc019-112">[in] Новое состояние для присвоения.</span><span class="sxs-lookup"><span data-stu-id="cc019-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="cc019-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="cc019-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="cc019-114">[in] Битоваяmas флагов, которая применяется к новому статусу и указывает флаги, которые необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="cc019-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="cc019-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="cc019-115">The following flags can be set:</span></span>
    
<span data-ttu-id="cc019-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="cc019-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="cc019-117">Сообщение помечено для удаления.</span><span class="sxs-lookup"><span data-stu-id="cc019-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="cc019-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="cc019-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="cc019-119">Сообщение не должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="cc019-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="cc019-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="cc019-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="cc019-121">Сообщение должно быть выделено.</span><span class="sxs-lookup"><span data-stu-id="cc019-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="cc019-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="cc019-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="cc019-123">Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="cc019-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="cc019-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="cc019-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="cc019-125">Сообщение помечено для скачивания из удаленного хранения сообщений в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="cc019-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="cc019-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="cc019-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="cc019-127">Сообщение помечено для определенной клиентом цели.</span><span class="sxs-lookup"><span data-stu-id="cc019-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="cc019-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="cc019-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="cc019-129">[out] Указатель на предыдущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc019-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc019-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc019-130">Return value</span></span>

<span data-ttu-id="cc019-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc019-131">S_OK</span></span> 
  
> <span data-ttu-id="cc019-132">Состояние сообщения успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="cc019-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc019-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc019-133">Remarks</span></span>

<span data-ttu-id="cc019-134">Метод **IMAPIFolder::SetMessageStatus** задает для состояния сообщения значение, которое хранится в его свойстве **PR_MSG_STATUS** ([PidTagMessageStatus).](pidtagmessagestatus-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cc019-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cc019-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="cc019-135">Notes to implementers</span></span>

<span data-ttu-id="cc019-136">Настройка, очистка и применение битов состояния сообщения полностью зависит от реализации, за исключением того, что биты от 0 до 15 зарезервированы и должны быть нулем.</span><span class="sxs-lookup"><span data-stu-id="cc019-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="cc019-137">Реализация этого метода удаленным поставщиком транспорта должна следовать семантике, описанной здесь.</span><span class="sxs-lookup"><span data-stu-id="cc019-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="cc019-138">Нет особых соображений.</span><span class="sxs-lookup"><span data-stu-id="cc019-138">There are no special considerations.</span></span> <span data-ttu-id="cc019-139">Клиенты используют этот метод для MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE, чтобы указать, что определенное сообщение необходимо скачать или удалить из удаленного хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc019-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="cc019-140">Поставщику удаленного транспорта не нужно реализовывать связанный метод [IMAPIFolder::GetMessageStatus.](imapifolder-getmessagestatus.md)</span><span class="sxs-lookup"><span data-stu-id="cc019-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="cc019-141">Клиенты должны найти в таблице содержимого папки состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc019-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cc019-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cc019-142">Notes to callers</span></span>

<span data-ttu-id="cc019-143">Вы можете использовать **PR_MSG_STATUS** сообщения для согласование операции блокировки сообщения с другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="cc019-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="cc019-144">Назначь бит в качестве бита блокировки.</span><span class="sxs-lookup"><span data-stu-id="cc019-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="cc019-145">Чтобы определить, задан ли бит блокировки, проверьте предыдущее значение состояния сообщения в параметре _lpulOldStatus._</span><span class="sxs-lookup"><span data-stu-id="cc019-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="cc019-146">Используйте другие биты в параметре  _ulNewStatus_ для отслеживания состояния сообщения, не мешив биту блокировки.</span><span class="sxs-lookup"><span data-stu-id="cc019-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc019-147">См. также</span><span class="sxs-lookup"><span data-stu-id="cc019-147">See also</span></span>



[<span data-ttu-id="cc019-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="cc019-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="cc019-149">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="cc019-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="cc019-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="cc019-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

