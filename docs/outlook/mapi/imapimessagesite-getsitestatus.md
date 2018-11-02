---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b804728541b0f2a0499bbf0078bfee2e5aed6ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563809"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="0602b-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="0602b-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="0602b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0602b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0602b-105">Возвращает сведения из объекта сайта сообщения о сообщении возможности веб-узла для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="0602b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0602b-106">Parameters</span></span>

 <span data-ttu-id="0602b-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="0602b-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="0602b-108">[out] Указатель на битовую маску флагов, который предоставляет сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="0602b-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="0602b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0602b-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="0602b-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="0602b-111">Можно скопировать сообщение.</span><span class="sxs-lookup"><span data-stu-id="0602b-111">The message can be copied.</span></span> 
    
<span data-ttu-id="0602b-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="0602b-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="0602b-113">Можно удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0602b-113">The message can be deleted.</span></span>
    
<span data-ttu-id="0602b-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="0602b-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="0602b-115">При удалении сообщения перемещаются в папку **Удаленных элементов** в хранилище сообщения вместо немедленно удаляется из его хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0602b-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="0602b-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="0602b-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="0602b-117">Можно перемещать сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-117">The message can be moved.</span></span>
    
<span data-ttu-id="0602b-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="0602b-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="0602b-119">Можно создать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="0602b-119">A new message can be created.</span></span>
    
<span data-ttu-id="0602b-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="0602b-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="0602b-121">Сообщения могут быть сохранены.</span><span class="sxs-lookup"><span data-stu-id="0602b-121">The message can be saved.</span></span>
    
<span data-ttu-id="0602b-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="0602b-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="0602b-123">Можно отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0602b-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0602b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0602b-124">Return value</span></span>

<span data-ttu-id="0602b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="0602b-125">S_OK</span></span> 
  
> <span data-ttu-id="0602b-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0602b-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0602b-127">���������</span><span class="sxs-lookup"><span data-stu-id="0602b-127">Remarks</span></span>

<span data-ttu-id="0602b-128">Объекты формы вызовите метод **IMAPIMessageSite::GetSiteStatus** , чтобы получить возможность объект сайта message для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="0602b-129">Флажки, возвращаемые в параметре _lpulStatus_ содержатся сведения о сайте сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="0602b-130">Как правило формы включает или отключает команды меню, в зависимости от сведений, флаги обеспечивают возможности реализации сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="0602b-131">Если новое сообщение загружается в форме, метод [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) или [IPersistMessage::Load](ipersistmessage-load.md) , проверяется состояние флаги.</span><span class="sxs-lookup"><span data-stu-id="0602b-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="0602b-132">Некоторые объекты сайта сообщения, особенно только для чтения, объектов, не разрешать сообщения, чтобы быть сохранены или удалены.</span><span class="sxs-lookup"><span data-stu-id="0602b-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0602b-133">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="0602b-133">Notes to implementers</span></span>

<span data-ttu-id="0602b-134">Метод **IMAPIMessageSite::GetSiteStatus** может потребоваться клиентское приложение для выполнения некоторых вычислений, чтобы определить, какие операции может или не может быть выполнена для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="0602b-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="0602b-135">Как правило, который включает в себя посмотрев в строке состояния для поставщика хранилища сообщений текущего сообщения или запросы поставщика хранилища, чтобы определить, какие действия в клиентском приложении можно выполнять с помощью хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0602b-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="0602b-136">Например, чтобы определить, нужно ли возвращать флаг MAPI_DELETE_IS_MOVE, проверьте свойство **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) объектов хранилища сообщений ли папки " **Удаленные** " в хранение сообщений.</span><span class="sxs-lookup"><span data-stu-id="0602b-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="0602b-137">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0602b-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0602b-138">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0602b-138">MFCMAPI reference</span></span>

<span data-ttu-id="0602b-139">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0602b-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0602b-140">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0602b-140">**File**</span></span>|<span data-ttu-id="0602b-141">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0602b-141">**Function**</span></span>|<span data-ttu-id="0602b-142">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0602b-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0602b-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0602b-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0602b-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="0602b-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="0602b-145">Mfcmapi (en) использует метод **IMAPIMessageSite::GetSiteStatus** , чтобы получить сведения о состоянии указанного сайта.</span><span class="sxs-lookup"><span data-stu-id="0602b-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="0602b-146">Он может вернуть VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE или VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="0602b-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0602b-147">См. также</span><span class="sxs-lookup"><span data-stu-id="0602b-147">See also</span></span>



[<span data-ttu-id="0602b-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="0602b-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="0602b-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="0602b-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="0602b-150">Каноническое свойство PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="0602b-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="0602b-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0602b-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="0602b-152">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="0602b-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0602b-153">Интерфейсы формы MAPI</span><span class="sxs-lookup"><span data-stu-id="0602b-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

