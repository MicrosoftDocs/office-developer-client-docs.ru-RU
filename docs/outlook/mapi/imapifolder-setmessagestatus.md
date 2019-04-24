---
title: Имапифолдерсетмессажестатус
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342779"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="11367-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="11367-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="11367-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11367-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11367-105">Задает состояние, связанное с сообщением (например, помечено ли это сообщение для удаления).</span><span class="sxs-lookup"><span data-stu-id="11367-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="11367-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11367-106">Parameters</span></span>

 <span data-ttu-id="11367-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="11367-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="11367-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="11367-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="11367-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="11367-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="11367-110">возврата Указатель на идентификатор записи для сообщения, состояние которого задано.</span><span class="sxs-lookup"><span data-stu-id="11367-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="11367-111">_Улневстатус_</span><span class="sxs-lookup"><span data-stu-id="11367-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="11367-112">возврата Новое состояние, которое будет назначено.</span><span class="sxs-lookup"><span data-stu-id="11367-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="11367-113">_Улневстатусмаск_</span><span class="sxs-lookup"><span data-stu-id="11367-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="11367-114">возврата Битовая маска флагов, которая применяется к новому статусу и указывает флаги, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="11367-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="11367-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="11367-115">The following flags can be set:</span></span>
    
<span data-ttu-id="11367-116">МСГСТАТУС_ДЕЛМАРКЕД</span><span class="sxs-lookup"><span data-stu-id="11367-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="11367-117">Сообщение помечено для удаления.</span><span class="sxs-lookup"><span data-stu-id="11367-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="11367-118">МСГСТАТУС_ХИДДЕН</span><span class="sxs-lookup"><span data-stu-id="11367-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="11367-119">Сообщение не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="11367-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="11367-120">МСГСТАТУС_ХИГХЛИГХТЕД</span><span class="sxs-lookup"><span data-stu-id="11367-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="11367-121">Сообщение будет отображаться выделенным.</span><span class="sxs-lookup"><span data-stu-id="11367-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="11367-122">МСГСТАТУС_РЕМОТЕ_ДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="11367-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="11367-123">Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки на локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="11367-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="11367-124">МСГСТАТУС_РЕМОТЕ_ДОВНЛОАД</span><span class="sxs-lookup"><span data-stu-id="11367-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="11367-125">Сообщение помечено для скачивания из удаленного хранилища сообщений в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="11367-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="11367-126">МСГСТАТУС_ТАГЖЕД</span><span class="sxs-lookup"><span data-stu-id="11367-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="11367-127">Сообщение было отмечено для определенного клиентом назначения.</span><span class="sxs-lookup"><span data-stu-id="11367-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="11367-128">_Лпулолдстатус_</span><span class="sxs-lookup"><span data-stu-id="11367-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="11367-129">вышли Указатель на предыдущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="11367-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11367-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11367-130">Return value</span></span>

<span data-ttu-id="11367-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="11367-131">S_OK</span></span> 
  
> <span data-ttu-id="11367-132">Состояние сообщения успешно задано.</span><span class="sxs-lookup"><span data-stu-id="11367-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11367-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11367-133">Remarks</span></span>

<span data-ttu-id="11367-134">Метод **IMAPIFolder:: сетмессажестатус** задает для состояния сообщения значение, хранящееся в его свойстве **пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11367-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="11367-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="11367-135">Notes to implementers</span></span>

<span data-ttu-id="11367-136">Как задаются, очищаются и используются биты состояния сообщения, полностью зависят от реализации, за исключением того, что биты от 0 до 15 зарезервированы и должны равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="11367-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="11367-137">Реализация этого метода У поставщика удаленного транспорта должна соответствовать семантике, описанной здесь.</span><span class="sxs-lookup"><span data-stu-id="11367-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="11367-138">Нет специальных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="11367-138">There are no special considerations.</span></span> <span data-ttu-id="11367-139">Клиенты используют этот метод, чтобы задать биты МСГСТАТУС_РЕМОТЕ_ДОВНЛОАД и МСГСТАТУС_РЕМОТЕ_ДЕЛЕТЕ, указывающие, что конкретное сообщение должно быть загружено или удалено из удаленного хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="11367-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="11367-140">Удаленный поставщик транспорта не должен реализовывать связанный метод [IMAPIFolder:: жетмессажестатус](imapifolder-getmessagestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="11367-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="11367-141">Клиенты должны выполнить поиск в таблице содержимого папки, чтобы определить состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="11367-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="11367-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="11367-142">Notes to callers</span></span>

<span data-ttu-id="11367-143">Вы можете использовать свойство **пр_мсг_статус** сообщения для согласования операции блокировки сообщений с другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="11367-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="11367-144">Назначьте бит блокировки.</span><span class="sxs-lookup"><span data-stu-id="11367-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="11367-145">Чтобы определить, установлен ли бит блокировки, изучите предыдущее значение состояния сообщения в параметре _лпулолдстатус_ .</span><span class="sxs-lookup"><span data-stu-id="11367-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="11367-146">Используйте другие биты в параметре _улневстатус_ для отслеживания состояния сообщений, не мешая битам блокировки.</span><span class="sxs-lookup"><span data-stu-id="11367-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11367-147">См. также</span><span class="sxs-lookup"><span data-stu-id="11367-147">See also</span></span>



[<span data-ttu-id="11367-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="11367-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="11367-149">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="11367-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="11367-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="11367-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

