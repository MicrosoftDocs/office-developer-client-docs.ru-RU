---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587847"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="84970-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="84970-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="84970-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84970-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84970-105">Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="84970-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="84970-106">���������</span><span class="sxs-lookup"><span data-stu-id="84970-106">Parameters</span></span>

 <span data-ttu-id="84970-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84970-107">_ulFlags_</span></span>
  
> <span data-ttu-id="84970-108">[in] Битовая маска флаги, который управляет параметром хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="84970-109">Следующие флаги являются взаимоисключающими; можно задать только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="84970-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="84970-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="84970-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="84970-111">Устанавливает хранилище сообщений по умолчанию сеанса.</span><span class="sxs-lookup"><span data-stu-id="84970-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="84970-112">Обновляет строку в таблице состояния хранилища сообщений, установив флажок STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84970-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="84970-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="84970-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="84970-114">Устанавливает хранилище сообщений в качестве хранилища для использования при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="84970-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="84970-115">Если хранилище сообщений не хранилище по умолчанию, клиенты должны сделать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="84970-116">Обновляет строку в таблице состояния хранилища сообщений, установив флажок STATUS_PRIMARY_STORE в столбце **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="84970-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="84970-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="84970-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="84970-118">Устанавливает хранилище сообщений в качестве хранилища для использования при входе в систему, если хранилище основных сообщений не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="84970-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="84970-119">Если клиент не может открыть основного хранилища, его открытие дополнительного хранилища и сохранить его как значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="84970-120">Обновляет строку в таблице состояния хранилища сообщений, установив флажок STATUS_SECONDARY_STORE в столбце **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="84970-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="84970-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="84970-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="84970-122">Задает флаг STATUS_SIMPLE_STORE в свойстве **PR_RESOURCE_FLAGS** хранилища сообщений, его состояние строки в таблице, строка таблицы хранилища сообщений, а в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="84970-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="84970-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="84970-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="84970-124">Задает флаг STATUS_SIMPLE_STORE в свойстве **PR_RESOURCE_FLAGS** хранилище сообщений в строке в таблице состояния и строка таблицы хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="84970-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="84970-125">Профиль не изменяется.</span><span class="sxs-lookup"><span data-stu-id="84970-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="84970-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="84970-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="84970-127">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="84970-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="84970-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="84970-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="84970-129">[in] Указатель на идентификатор записи хранилища сообщений, предназначенного по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="84970-130">Если клиент передает значение NULL в _lpEntryID_, без хранилища сообщений будет установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84970-131">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="84970-131">Return value</span></span>

<span data-ttu-id="84970-132">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="84970-132">S_OK</span></span> 
  
> <span data-ttu-id="84970-133">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="84970-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84970-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="84970-134">Remarks</span></span>

<span data-ttu-id="84970-135">Метод **IMAPISession::SetDefaultStore** устанавливает хранилища сообщений как один из следующих:</span><span class="sxs-lookup"><span data-stu-id="84970-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="84970-136">Хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="84970-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="84970-137">Хранилище основных сообщений для сеанса.</span><span class="sxs-lookup"><span data-stu-id="84970-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="84970-138">Хранилище дополнительного сообщения для сеанса.</span><span class="sxs-lookup"><span data-stu-id="84970-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="84970-139">Чтобы установить хранилище сообщений по умолчанию, хранилища сообщений необходимо иметь следующие флаги, задайте в своем свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="84970-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="84970-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="84970-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="84970-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="84970-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="84970-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="84970-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="84970-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="84970-143">Notes to callers</span></span>

<span data-ttu-id="84970-144">Можно определить хранилище сообщений по умолчанию для сеанса, получение состояния и поиск состояние флага STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="84970-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="84970-145">Строку, которая содержит этот параметр представляет хранилища сообщений, которое используется в качестве сеанса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="84970-146">Если MAPI_DEFAULT_STORE или флаг MAPI_SIMPLE_STORE_PERMANENT, MAPI обновляет профилей, таблицы хранилища сообщений и состояния в таблице.</span><span class="sxs-lookup"><span data-stu-id="84970-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="84970-147">При внесении изменений в хранилище сообщений по умолчанию, создаются следующие уведомления:</span><span class="sxs-lookup"><span data-stu-id="84970-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="84970-148">Уведомление о событии **fnevTableModified** отправляется для каждой затронутых строки в обоих хранилища и состояние таблицы сообщений.</span><span class="sxs-lookup"><span data-stu-id="84970-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="84970-149">Внутренних уведомлений отправляется в очередь MAPI.</span><span class="sxs-lookup"><span data-stu-id="84970-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="84970-150">Операции в уже начатую завершены без изменения; новые операций на хранилище сообщений по умолчанию, например загрузку сообщений обрабатываются для новое хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="84970-151">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="84970-151">MFCMAPI reference</span></span>

<span data-ttu-id="84970-152">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="84970-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84970-153">**����**</span><span class="sxs-lookup"><span data-stu-id="84970-153">**File**</span></span>|<span data-ttu-id="84970-154">**�������**</span><span class="sxs-lookup"><span data-stu-id="84970-154">**Function**</span></span>|<span data-ttu-id="84970-155">**�����������**</span><span class="sxs-lookup"><span data-stu-id="84970-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84970-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="84970-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="84970-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="84970-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="84970-158">Mfcmapi (en) используется метод **IMAPISession::SetDefaultStore** для определения выбранного магазина как хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84970-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84970-159">См. также</span><span class="sxs-lookup"><span data-stu-id="84970-159">See also</span></span>



[<span data-ttu-id="84970-160">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="84970-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="84970-161">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="84970-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="84970-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="84970-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="84970-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="84970-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="84970-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="84970-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

