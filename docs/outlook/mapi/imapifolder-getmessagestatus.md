---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418640"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="74221-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="74221-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="74221-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74221-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74221-105">Получает состояние, связанное с сообщением в определенной папке (например, помечено ли это сообщение для удаления).</span><span class="sxs-lookup"><span data-stu-id="74221-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="74221-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="74221-106">Parameters</span></span>

 <span data-ttu-id="74221-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="74221-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="74221-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="74221-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="74221-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="74221-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="74221-110">[in] Указатель на идентификатор записи для сообщения, состояние которого получено.</span><span class="sxs-lookup"><span data-stu-id="74221-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="74221-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74221-111">_ulFlags_</span></span>
  
> <span data-ttu-id="74221-112">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="74221-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="74221-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="74221-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="74221-114">[вышел] Указатель на указатель на битмаску флагов, указываю на состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="74221-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="74221-115">Биты от 0 до 15 зарезервированы и должны быть нулем; биты от 16 до 31 доступны для реализации.</span><span class="sxs-lookup"><span data-stu-id="74221-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="74221-116">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="74221-116">The following flags can be set:</span></span>
    
<span data-ttu-id="74221-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="74221-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="74221-118">Сообщение помечено для удаления.</span><span class="sxs-lookup"><span data-stu-id="74221-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="74221-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="74221-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="74221-120">Сообщение не отображается.</span><span class="sxs-lookup"><span data-stu-id="74221-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="74221-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="74221-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="74221-122">Сообщение должно отображаться выделено.</span><span class="sxs-lookup"><span data-stu-id="74221-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="74221-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="74221-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="74221-124">Сообщение помечено для удаления в хранилище удаленных сообщений без загрузки в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="74221-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="74221-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="74221-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="74221-126">Сообщение помечено для скачивания из удаленного магазина сообщений в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="74221-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="74221-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="74221-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="74221-128">Сообщение помечено для определенной клиентом цели.</span><span class="sxs-lookup"><span data-stu-id="74221-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74221-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74221-129">Return value</span></span>

<span data-ttu-id="74221-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="74221-130">S_OK</span></span> 
  
> <span data-ttu-id="74221-131">Состояние сообщения было успешно восстановлено.</span><span class="sxs-lookup"><span data-stu-id="74221-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74221-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="74221-132">Remarks</span></span>

<span data-ttu-id="74221-133">Метод **IMAPIFolder::GetMessageStatus** возвращает состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="74221-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="74221-134">Состояние сообщения хранится в свойстве **PR_MSG_STATUS** [(PidTagMessageStatus).](pidtagmessagestatus-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="74221-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="74221-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="74221-135">Notes to implementers</span></span>

<span data-ttu-id="74221-136">Настройка, очистка и применение битов состояния сообщений полностью зависит от реализации, за исключением того, что биты от 0 до 15 зарезервированы и должны быть нулем.</span><span class="sxs-lookup"><span data-stu-id="74221-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="74221-137">Если вы сохраняете сообщения в подтрите IPM, MAPI зарезервировать биты от 16 до 31 для использования клиентами IPM.</span><span class="sxs-lookup"><span data-stu-id="74221-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="74221-138">Если вы сохраняете сообщения в других подтриях, вы можете использовать биты от 16 до 31 для собственных целей.</span><span class="sxs-lookup"><span data-stu-id="74221-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="74221-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="74221-139">MFCMAPI reference</span></span>

<span data-ttu-id="74221-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="74221-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="74221-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="74221-141">**File**</span></span>|<span data-ttu-id="74221-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="74221-142">**Function**</span></span>|<span data-ttu-id="74221-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="74221-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74221-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="74221-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="74221-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="74221-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="74221-146">MFCMAPI использует **метод IMAPIFolder::GetMessageStatus** для получения состояния следующего сообщения, которое будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="74221-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="74221-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="74221-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="74221-148">OpenMessageNonModal и OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="74221-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="74221-149">MFCMAPI использует метод **IMAPIFolder::GetMessageStatus,** чтобы получить состояние сообщения, отображаемого для просмотра форм, который является CMyMAPIFormViewer или [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="74221-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74221-150">См. также</span><span class="sxs-lookup"><span data-stu-id="74221-150">See also</span></span>



[<span data-ttu-id="74221-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="74221-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="74221-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="74221-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="74221-153">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="74221-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="74221-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="74221-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="74221-155">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="74221-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

