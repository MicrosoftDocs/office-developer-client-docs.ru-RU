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
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414384"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="27b50-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="27b50-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="27b50-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27b50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27b50-105">Пытается удалить сообщение из исходя такой очереди.</span><span class="sxs-lookup"><span data-stu-id="27b50-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="27b50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27b50-106">Parameters</span></span>

 <span data-ttu-id="27b50-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="27b50-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="27b50-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="27b50-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="27b50-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="27b50-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="27b50-110">[in] Указатель на идентификатор записи сообщения, удаляемого из исходяской очереди.</span><span class="sxs-lookup"><span data-stu-id="27b50-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="27b50-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27b50-111">_ulFlags_</span></span>
  
> <span data-ttu-id="27b50-112">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="27b50-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27b50-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27b50-113">Return value</span></span>

<span data-ttu-id="27b50-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="27b50-114">S_OK</span></span> 
  
> <span data-ttu-id="27b50-115">Сообщение успешно удалено из исходяной очереди.</span><span class="sxs-lookup"><span data-stu-id="27b50-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="27b50-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="27b50-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="27b50-117">Сообщение, определенное  _lpEntryID,_ больше не находится в очереди исходяющих сообщений, как правило, так как оно уже отправлено.</span><span class="sxs-lookup"><span data-stu-id="27b50-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="27b50-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="27b50-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="27b50-119">Сообщение, идентифицированное  _lpEntryID,_ заблокировано пулом MAPI, и операцию нельзя прерывать.</span><span class="sxs-lookup"><span data-stu-id="27b50-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="27b50-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="27b50-120">Remarks</span></span>

<span data-ttu-id="27b50-121">Метод **IMsgStore::AbortSubmit** пытается удалить отправленное сообщение из исходявой очереди хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="27b50-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="27b50-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="27b50-122">Notes to callers</span></span>

<span data-ttu-id="27b50-123">После отправки сообщения единственным действием, которое может быть выполнено с сообщением, является прекращение отправки путем вызова **AbortSubmit.**</span><span class="sxs-lookup"><span data-stu-id="27b50-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="27b50-124">Не **ожидайте, что abortSubmit** всегда будет успешным.</span><span class="sxs-lookup"><span data-stu-id="27b50-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="27b50-125">В зависимости от того, как реализована система обмена сообщениями, отменить отправку сообщения может быть невозможно.</span><span class="sxs-lookup"><span data-stu-id="27b50-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="27b50-126">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="27b50-126">MFCMAPI reference</span></span>

<span data-ttu-id="27b50-127">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="27b50-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="27b50-128">**Файл**</span><span class="sxs-lookup"><span data-stu-id="27b50-128">**File**</span></span>|<span data-ttu-id="27b50-129">**Функция**</span><span class="sxs-lookup"><span data-stu-id="27b50-129">**Function**</span></span>|<span data-ttu-id="27b50-130">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="27b50-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27b50-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="27b50-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="27b50-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="27b50-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="27b50-133">MFCMAPI использует метод **IMsgStore::AbortSubmit,** чтобы отменить отправку выбранного сообщения.</span><span class="sxs-lookup"><span data-stu-id="27b50-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27b50-134">См. также</span><span class="sxs-lookup"><span data-stu-id="27b50-134">See also</span></span>



[<span data-ttu-id="27b50-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="27b50-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="27b50-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="27b50-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="27b50-137">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="27b50-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

