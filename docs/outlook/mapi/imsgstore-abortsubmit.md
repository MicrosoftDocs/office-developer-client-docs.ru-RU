---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809384"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="4bdc3-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="4bdc3-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="4bdc3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4bdc3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4bdc3-105">Пытается удалить сообщения из очереди исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4bdc3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bdc3-106">Parameters</span></span>

 <span data-ttu-id="4bdc3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4bdc3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4bdc3-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4bdc3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4bdc3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4bdc3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4bdc3-110">[in] Указатель на идентификатор записи сообщения для удаления из очереди исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="4bdc3-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4bdc3-111">_ulFlags_</span></span>
  
> <span data-ttu-id="4bdc3-112">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4bdc3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3">Return value</span></span>

<span data-ttu-id="4bdc3-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4bdc3-114">S_OK</span></span> 
  
> <span data-ttu-id="4bdc3-115">Сообщение успешно удалено из исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="4bdc3-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="4bdc3-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="4bdc3-117">Сообщение, определяемую средством _lpEntryID_ больше не в хранилище сообщений исходящей очереди, как правило, так как он уже был отправлен.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="4bdc3-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="4bdc3-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="4bdc3-119">Сообщение, определяемую средством _lpEntryID_ заблокирована диспетчером очереди MAPI, операция не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4bdc3-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="4bdc3-120">Remarks</span></span>

<span data-ttu-id="4bdc3-121">Метод **IMsgStore::AbortSubmit** пытается удалить отправленное сообщение из очереди исходящих хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4bdc3-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4bdc3-122">Notes to callers</span></span>

<span data-ttu-id="4bdc3-123">После отправки сообщения прерывание подачи путем вызова **AbortSubmit** — это единственный действие, которое может выполняться в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="4bdc3-124">Не ожидается **AbortSubmit** всегда выполняются успешно.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="4bdc3-125">В зависимости от того, как реализуется системы обмена сообщениями может оказаться невозможно отменить отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4bdc3-126">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="4bdc3-126">MFCMAPI reference</span></span>

<span data-ttu-id="4bdc3-127">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4bdc3-128">**����**</span><span class="sxs-lookup"><span data-stu-id="4bdc3-128">**File**</span></span>|<span data-ttu-id="4bdc3-129">**�������**</span><span class="sxs-lookup"><span data-stu-id="4bdc3-129">**Function**</span></span>|<span data-ttu-id="4bdc3-130">**�����������**</span><span class="sxs-lookup"><span data-stu-id="4bdc3-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4bdc3-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="4bdc3-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="4bdc3-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="4bdc3-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="4bdc3-133">Mfcmapi (en) использует метод **IMsgStore::AbortSubmit** для прекращения предоставления выбранного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4bdc3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4bdc3-134">See also</span></span>



[<span data-ttu-id="4bdc3-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="4bdc3-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="4bdc3-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4bdc3-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="4bdc3-137">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="4bdc3-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

