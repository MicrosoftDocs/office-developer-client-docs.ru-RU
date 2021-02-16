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
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426109"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="59147-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="59147-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="59147-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59147-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59147-105">Устанавливает хранилище сообщений как хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="59147-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="59147-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59147-106">Parameters</span></span>

 <span data-ttu-id="59147-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59147-107">_ulFlags_</span></span>
  
> <span data-ttu-id="59147-108">[in] Битоваяmas флагов, которая управляет настройкой хранения сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="59147-109">Эти флаги являются взаимоисключающими; Можно установить только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="59147-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="59147-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="59147-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="59147-111">Устанавливает хранилище сообщений в качестве сеанса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="59147-112">Обновляет строку таблицы состояния в хранилище сообщений, устанавливая флаг STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="59147-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="59147-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="59147-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="59147-114">Устанавливает хранилище сообщений как хранилище, которое будет использоваться при logon.</span><span class="sxs-lookup"><span data-stu-id="59147-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="59147-115">Если хранилище сообщений не является хранилищем по умолчанию, клиенты должны сделать его хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="59147-116">Обновляет строку таблицы состояния в хранилище сообщений, устанавливая флаг STATUS_PRIMARY_STORE в столбце **PR_RESOURCE_FLAGS** сообщений.</span><span class="sxs-lookup"><span data-stu-id="59147-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="59147-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="59147-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="59147-118">Устанавливает хранилище сообщений как хранилище, которое будет использоваться при logon, если основное хранилище сообщений не доступно.</span><span class="sxs-lookup"><span data-stu-id="59147-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="59147-119">Если клиенту не удается открыть основное хранилище, он должен открыть дополнительное хранилище и установить его по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="59147-120">Обновляет строку таблицы состояния в хранилище сообщений, устанавливая флаг STATUS_SECONDARY_STORE в столбце **PR_RESOURCE_FLAGS** сообщений.</span><span class="sxs-lookup"><span data-stu-id="59147-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="59147-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="59147-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="59147-122">Задает флаг STATUS_SIMPLE_STORE в свойстве PR_RESOURCE_FLAGS хранения сообщений в строке **таблицы состояния,** строке таблицы для хранения сообщений и профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="59147-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="59147-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="59147-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="59147-124">Задает флаг STATUS_SIMPLE_STORE в свойстве PR_RESOURCE_FLAGS хранения сообщений в строке **таблицы состояния** и строке таблицы для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="59147-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="59147-125">Профиль не изменен.</span><span class="sxs-lookup"><span data-stu-id="59147-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="59147-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="59147-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="59147-127">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="59147-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="59147-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="59147-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="59147-129">[in] Указатель на идентификатор записи в хранилище сообщений, который предназначен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="59147-130">Если клиент передает значение NULL в  _lpEntryID,_ хранилище сообщений не выбрано по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59147-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59147-131">Return value</span></span>

<span data-ttu-id="59147-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="59147-132">S_OK</span></span> 
  
> <span data-ttu-id="59147-133">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="59147-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59147-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="59147-134">Remarks</span></span>

<span data-ttu-id="59147-135">Метод **IMAPISession::SetDefaultStore** создает хранилище сообщений как одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="59147-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="59147-136">Хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="59147-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="59147-137">Основное хранилище сообщений для сеанса.</span><span class="sxs-lookup"><span data-stu-id="59147-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="59147-138">Дополнительное хранилище сообщений для сеанса.</span><span class="sxs-lookup"><span data-stu-id="59147-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="59147-139">Чтобы установить хранилище сообщений по умолчанию, в свойстве **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)должны быть установлены следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="59147-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="59147-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="59147-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="59147-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="59147-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="59147-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="59147-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="59147-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="59147-143">Notes to callers</span></span>

<span data-ttu-id="59147-144">Чтобы определить хранилище сообщений по умолчанию для сеанса, необходимо получить таблицу состояния и найти параметр флага STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS.**</span><span class="sxs-lookup"><span data-stu-id="59147-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="59147-145">Строка с этим параметром представляет хранилище сообщений, назначенное по умолчанию сеансом.</span><span class="sxs-lookup"><span data-stu-id="59147-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="59147-146">Если установлен MAPI_DEFAULT_STORE или MAPI_SIMPLE_STORE_PERMANENT, MAPI обновляет профиль, таблицу хранения сообщений и таблицу состояния.</span><span class="sxs-lookup"><span data-stu-id="59147-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="59147-147">При изменении параметра по умолчанию для хранения сообщений создаются следующие уведомления:</span><span class="sxs-lookup"><span data-stu-id="59147-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="59147-148">Уведомление **о событии fnevTableModified** выдано для каждой затронутой строки как в хранилище сообщений, так и в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="59147-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="59147-149">Для пула MAPI выдано внутреннее уведомление.</span><span class="sxs-lookup"><span data-stu-id="59147-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="59147-150">Операции, которые уже находятся в процессе выполнения, завершались без изменений; новые операции, которые включают хранилище сообщений по умолчанию, например загрузку сообщений, обрабатываются для нового магазина по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="59147-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="59147-151">MFCMAPI reference</span></span>

<span data-ttu-id="59147-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="59147-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="59147-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="59147-153">**File**</span></span>|<span data-ttu-id="59147-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="59147-154">**Function**</span></span>|<span data-ttu-id="59147-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="59147-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59147-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="59147-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="59147-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="59147-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="59147-158">MFCMAPI использует метод **IMAPISession::SetDefaultStore,** чтобы установить выбранное хранилище как хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59147-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59147-159">См. также</span><span class="sxs-lookup"><span data-stu-id="59147-159">See also</span></span>



[<span data-ttu-id="59147-160">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="59147-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="59147-161">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="59147-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="59147-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="59147-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="59147-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="59147-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="59147-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="59147-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

