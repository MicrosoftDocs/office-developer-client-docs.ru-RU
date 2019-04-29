---
title: Имапимессажеситежетситестатус
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
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="d6860-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d6860-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="d6860-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6860-105">Возвращает сведения из объекта сайта сообщения о возможностях сайта сообщения для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6860-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="d6860-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6860-106">Parameters</span></span>

 <span data-ttu-id="d6860-107">_Лпулстатус_</span><span class="sxs-lookup"><span data-stu-id="d6860-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="d6860-108">вышли Указатель на битовую маску флагов, которая предоставляет сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6860-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="d6860-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d6860-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d6860-110">ВКСТАТУС_КОПИ</span><span class="sxs-lookup"><span data-stu-id="d6860-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="d6860-111">Сообщение может быть скопировано.</span><span class="sxs-lookup"><span data-stu-id="d6860-111">The message can be copied.</span></span> 
    
<span data-ttu-id="d6860-112">ВКСТАТУС_ДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="d6860-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="d6860-113">Сообщение может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="d6860-113">The message can be deleted.</span></span>
    
<span data-ttu-id="d6860-114">ВКСТАТУС_ДЕЛЕТЕ_ИС_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="d6860-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="d6860-115">При удалении сообщение перемещается в папку " **Удаленные** " в своем хранилище сообщений, а не сразу удаляется из его хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6860-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="d6860-116">ВКСТАТУС_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="d6860-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="d6860-117">Сообщение может быть перемещено.</span><span class="sxs-lookup"><span data-stu-id="d6860-117">The message can be moved.</span></span>
    
<span data-ttu-id="d6860-118">ВКСТАТУС_НЕВ_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="d6860-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="d6860-119">Можно создать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="d6860-119">A new message can be created.</span></span>
    
<span data-ttu-id="d6860-120">ВКСТАТУС_САВЕ</span><span class="sxs-lookup"><span data-stu-id="d6860-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="d6860-121">Сообщение может быть сохранено.</span><span class="sxs-lookup"><span data-stu-id="d6860-121">The message can be saved.</span></span>
    
<span data-ttu-id="d6860-122">ВКСТАТУС_СУБМИТ</span><span class="sxs-lookup"><span data-stu-id="d6860-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="d6860-123">Сообщение может быть отправлено.</span><span class="sxs-lookup"><span data-stu-id="d6860-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6860-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6860-124">Return value</span></span>

<span data-ttu-id="d6860-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6860-125">S_OK</span></span> 
  
> <span data-ttu-id="d6860-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d6860-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6860-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6860-127">Remarks</span></span>

<span data-ttu-id="d6860-128">Объекты формы вызывают метод **имапимессажесите:: жетситестатус** для получения возможностей объекта сайта сообщения для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6860-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="d6860-129">Флаги, возвращаемые в параметре _лпулстатус_ , предоставляют сведения о сайте сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6860-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="d6860-130">Как правило, форма включает или отключает команды меню, в зависимости от информации, которая предоставляет пометки о возможностях реализации сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6860-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="d6860-131">Если новое сообщение загружается в форму с помощью метода [иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) или [Иперсистмессаже:: Load](ipersistmessage-load.md) , необходимо проверить флаги состояния.</span><span class="sxs-lookup"><span data-stu-id="d6860-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="d6860-132">Некоторые объекты сайта сообщений, особенно объекты, предназначенные только для чтения, не допускают сохранения и удаления сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6860-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d6860-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d6860-133">Notes to implementers</span></span>

<span data-ttu-id="d6860-134">В методе **имапимессажесите:: жетситестатус** может потребоваться, чтобы клиентское приложение выполняло некоторые вычисления, чтобы определить, какие операции можно или невозможно выполнить с текущим сообщением.</span><span class="sxs-lookup"><span data-stu-id="d6860-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="d6860-135">Как правило, при просмотре строки состояния для поставщика хранилища сообщений текущего сообщения или запроса к поставщику магазина, чтобы определить, какие действия клиентское приложение может выполнять с помощью хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6860-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="d6860-136">Например, чтобы определить, возвращать ли флаг МАПИ_ДЕЛЕТЕ_ИС_МОВЕ, проверьте свойство \*\*пр_ипм_вастебаскет_ентрид\*\* объекта хранилища сообщений ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)), чтобы узнать, есть ли папка " **Удаленные** " в папке хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6860-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="d6860-137">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d6860-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6860-138">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d6860-138">MFCMAPI reference</span></span>

<span data-ttu-id="d6860-139">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d6860-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6860-140">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d6860-140">**File**</span></span>|<span data-ttu-id="d6860-141">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d6860-141">**Function**</span></span>|<span data-ttu-id="d6860-142">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d6860-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6860-143">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="d6860-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d6860-144">Кмимапиформвиевер:: Жетситестатус</span><span class="sxs-lookup"><span data-stu-id="d6860-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="d6860-145">MFCMAPI использует метод **имапимессажесите:: жетситестатус** для получения состояния указанного сайта.</span><span class="sxs-lookup"><span data-stu-id="d6860-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="d6860-146">Он может возвращать ВКСТАТУС_НЕВ_МЕССАЖЕ, ВКСТАТУС_САВЕ или ВКСТАТУС_СУБМИТ.</span><span class="sxs-lookup"><span data-stu-id="d6860-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6860-147">См. также</span><span class="sxs-lookup"><span data-stu-id="d6860-147">See also</span></span>



[<span data-ttu-id="d6860-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="d6860-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="d6860-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="d6860-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="d6860-150">Каноническое свойство PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="d6860-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="d6860-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6860-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d6860-152">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="d6860-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d6860-153">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="d6860-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

