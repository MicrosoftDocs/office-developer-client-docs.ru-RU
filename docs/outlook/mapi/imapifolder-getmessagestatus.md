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
ms.openlocfilehash: 8e5ccadbd6df664b6650487f340508ae4548a1c2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583269"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="2924e-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="2924e-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="2924e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2924e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2924e-105">Получение сведений о состоянии, связанные с сообщение в определенной папке (например, будет ли это сообщение помечено для удаления).</span><span class="sxs-lookup"><span data-stu-id="2924e-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="2924e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2924e-106">Parameters</span></span>

 <span data-ttu-id="2924e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2924e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2924e-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2924e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2924e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2924e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2924e-110">[in] Указатель на идентификатор записи для сообщения, состояние которого получается.</span><span class="sxs-lookup"><span data-stu-id="2924e-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="2924e-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2924e-111">_ulFlags_</span></span>
  
> <span data-ttu-id="2924e-112">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="2924e-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2924e-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="2924e-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="2924e-114">[out] Указатель на указатель битовой маски флагов, которые указывают состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="2924e-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="2924e-115">Цифры от 0 до 15 бит зарезервированы и должно быть равно нулю; бит 16 до 31 доступны для использования реализации.</span><span class="sxs-lookup"><span data-stu-id="2924e-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="2924e-116">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="2924e-116">The following flags can be set:</span></span>
    
<span data-ttu-id="2924e-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="2924e-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="2924e-118">Сообщение было помечено для удаления.</span><span class="sxs-lookup"><span data-stu-id="2924e-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="2924e-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="2924e-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="2924e-120">Сообщение является не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="2924e-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="2924e-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="2924e-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="2924e-122">Это сообщение будет отображаться выделенный.</span><span class="sxs-lookup"><span data-stu-id="2924e-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="2924e-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="2924e-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="2924e-124">Сообщение было помечено для удаления в магазине удаленных сообщений без загрузки локального клиента.</span><span class="sxs-lookup"><span data-stu-id="2924e-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="2924e-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="2924e-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="2924e-126">Сообщение было помечено для загрузки с хранения удаленных сообщений для локального клиента.</span><span class="sxs-lookup"><span data-stu-id="2924e-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="2924e-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="2924e-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="2924e-128">Сообщение уже помечен для определенного клиента цели.</span><span class="sxs-lookup"><span data-stu-id="2924e-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2924e-129">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2924e-129">Return value</span></span>

<span data-ttu-id="2924e-130">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2924e-130">S_OK</span></span> 
  
> <span data-ttu-id="2924e-131">Состояние сообщения был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="2924e-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2924e-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="2924e-132">Remarks</span></span>

<span data-ttu-id="2924e-133">Метод **IMAPIFolder::GetMessageStatus** возвращает состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="2924e-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="2924e-134">Состояние сообщения хранится в свойстве **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщение.</span><span class="sxs-lookup"><span data-stu-id="2924e-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2924e-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2924e-135">Notes to implementers</span></span>

<span data-ttu-id="2924e-136">Как задать, снят и используется биты состояния сообщение полностью зависит от реализации, за исключением того, что бит 0 до 15 зарезервированы и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2924e-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="2924e-137">При сохранении сообщения в поддерева IPM MAPI оставляет за собой биты 16 до 31 для использования клиентами IPM.</span><span class="sxs-lookup"><span data-stu-id="2924e-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="2924e-138">Если хранение сообщений в другие поддеревьев, можно использовать бит 16 до 31 для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="2924e-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2924e-139">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="2924e-139">MFCMAPI reference</span></span>

<span data-ttu-id="2924e-140">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="2924e-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2924e-141">**����**</span><span class="sxs-lookup"><span data-stu-id="2924e-141">**File**</span></span>|<span data-ttu-id="2924e-142">**�������**</span><span class="sxs-lookup"><span data-stu-id="2924e-142">**Function**</span></span>|<span data-ttu-id="2924e-143">**�����������**</span><span class="sxs-lookup"><span data-stu-id="2924e-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2924e-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="2924e-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="2924e-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="2924e-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="2924e-146">Mfcmapi (en) использует метод **IMAPIFolder::GetMessageStatus** , чтобы получить сведения о состоянии следующее сообщение для отображения.</span><span class="sxs-lookup"><span data-stu-id="2924e-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="2924e-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2924e-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2924e-148">OpenMessageNonModal и OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="2924e-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="2924e-149">Mfcmapi (en) использует метод **IMAPIFolder::GetMessageStatus** , чтобы получить сведения о состоянии сообщение, отображаемое для передачи для просмотра формы, который является CMyMAPIFormViewer или [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="2924e-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2924e-150">См. также</span><span class="sxs-lookup"><span data-stu-id="2924e-150">See also</span></span>



[<span data-ttu-id="2924e-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="2924e-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="2924e-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="2924e-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="2924e-153">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="2924e-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="2924e-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2924e-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="2924e-155">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2924e-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

