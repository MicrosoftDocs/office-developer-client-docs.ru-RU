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
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430128"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="6a23b-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="6a23b-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="6a23b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a23b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a23b-105">Возвращает сведения из объекта сайта сообщения о возможностях сайта сообщений для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a23b-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="6a23b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a23b-106">Parameters</span></span>

 <span data-ttu-id="6a23b-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="6a23b-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="6a23b-108">[out] Указатель на битовуюmass флагов, которая предоставляет сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a23b-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="6a23b-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6a23b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="6a23b-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="6a23b-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="6a23b-111">Сообщение можно скопировать.</span><span class="sxs-lookup"><span data-stu-id="6a23b-111">The message can be copied.</span></span> 
    
<span data-ttu-id="6a23b-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="6a23b-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="6a23b-113">Сообщение можно удалить.</span><span class="sxs-lookup"><span data-stu-id="6a23b-113">The message can be deleted.</span></span>
    
<span data-ttu-id="6a23b-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="6a23b-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="6a23b-115">При удалении сообщение перемещается  в папку "Удаленные" в хранилище сообщений вместо немедленного удаления из него.</span><span class="sxs-lookup"><span data-stu-id="6a23b-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="6a23b-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="6a23b-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="6a23b-117">Сообщение может быть перемещено.</span><span class="sxs-lookup"><span data-stu-id="6a23b-117">The message can be moved.</span></span>
    
<span data-ttu-id="6a23b-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="6a23b-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="6a23b-119">Можно создать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="6a23b-119">A new message can be created.</span></span>
    
<span data-ttu-id="6a23b-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="6a23b-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="6a23b-121">Сообщение можно сохранить.</span><span class="sxs-lookup"><span data-stu-id="6a23b-121">The message can be saved.</span></span>
    
<span data-ttu-id="6a23b-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="6a23b-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="6a23b-123">Сообщение может быть отправлено.</span><span class="sxs-lookup"><span data-stu-id="6a23b-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a23b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a23b-124">Return value</span></span>

<span data-ttu-id="6a23b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a23b-125">S_OK</span></span> 
  
> <span data-ttu-id="6a23b-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6a23b-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a23b-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a23b-127">Remarks</span></span>

<span data-ttu-id="6a23b-128">Объекты форм вызовите метод **IMAPIMessageSite::GetSiteStatus,** чтобы получить возможности объекта сайта сообщения для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a23b-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="6a23b-129">Флаги, возвращенные в  _параметре lpulStatus,_ предоставляют сведения о сайте сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a23b-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="6a23b-130">Как правило, форма включает или отключает команды меню в зависимости от сведений, которые флаги предоставляют о возможностях реализации сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a23b-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="6a23b-131">Если новое сообщение загружается в форму методом [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) или [методом IPersistMessage::Load,](ipersistmessage-load.md) необходимо проверить флаги состояния.</span><span class="sxs-lookup"><span data-stu-id="6a23b-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="6a23b-132">Некоторые объекты сайта сообщений, особенно объекты только для чтения, не позволяют сохранить или удалить сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a23b-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6a23b-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6a23b-133">Notes to implementers</span></span>

<span data-ttu-id="6a23b-134">Метод **IMAPIMessageSite::GetSiteStatus** может потребовать от клиентского приложения выполнить некоторые вычисления, чтобы определить, какие операции могут выполняться или не могут выполняться с текущим сообщением.</span><span class="sxs-lookup"><span data-stu-id="6a23b-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="6a23b-135">Как правило, это связано с просмотром строки состояния поставщика текущего магазина сообщений или запросом у поставщика магазина, чтобы определить, какие действия может выполнять клиентская приложение с помощью этого магазина.</span><span class="sxs-lookup"><span data-stu-id="6a23b-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="6a23b-136">Например, чтобы определить, следует ли возвращать флаг MAPI_DELETE_IS_MOVE, проверьте свойство **PR_IPM_WASTEBASKET_ENTRYID** объекта PR_IPM_WASTEBASKET_ENTRYID [(PidTagIpmWastebasketEntryId),](pidtagipmwastebasketentryid-canonical-property.md)чтобы узнать,  есть ли в хранилище сообщений папка "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="6a23b-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="6a23b-137">Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="6a23b-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6a23b-138">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6a23b-138">MFCMAPI reference</span></span>

<span data-ttu-id="6a23b-139">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6a23b-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6a23b-140">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6a23b-140">**File**</span></span>|<span data-ttu-id="6a23b-141">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6a23b-141">**Function**</span></span>|<span data-ttu-id="6a23b-142">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6a23b-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6a23b-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="6a23b-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6a23b-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="6a23b-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="6a23b-145">MFCMAPI использует метод **IMAPIMessageSite::GetSiteStatus** для получения состояния указанного сайта.</span><span class="sxs-lookup"><span data-stu-id="6a23b-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="6a23b-146">Он может возвращать VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE или VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="6a23b-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a23b-147">См. также</span><span class="sxs-lookup"><span data-stu-id="6a23b-147">See also</span></span>



[<span data-ttu-id="6a23b-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="6a23b-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="6a23b-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="6a23b-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="6a23b-150">Каноническое свойство PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="6a23b-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="6a23b-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a23b-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="6a23b-152">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="6a23b-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6a23b-153">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="6a23b-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

