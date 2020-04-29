---
title: имаписессионсетдефаултсторе
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
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="822b3-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="822b3-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="822b3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="822b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="822b3-105">Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="822b3-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="822b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="822b3-106">Parameters</span></span>

 <span data-ttu-id="822b3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="822b3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="822b3-108">возврата Битовая маска флагов, которые управляют параметром хранилища сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="822b3-109">Эти флаги являются взаимоисключающими; можно задать только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="822b3-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="822b3-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="822b3-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="822b3-111">Задает хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="822b3-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="822b3-112">Обновляет строку таблицы состояния хранилища сообщений, устанавливая флаг STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="822b3-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="822b3-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="822b3-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="822b3-114">Создает хранилище сообщений в качестве хранилища, которое будет использоваться при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="822b3-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="822b3-115">Если хранилище сообщений не является хранилищем по умолчанию, клиенты должны сделать его значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="822b3-116">Обновляет строку таблицы состояния хранилища сообщений, устанавливая флаг STATUS_PRIMARY_STORE в столбце **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="822b3-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="822b3-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="822b3-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="822b3-118">Создает хранилище сообщений в качестве хранилища, которое будет использоваться при входе в систему, если основное хранилище сообщений недоступно.</span><span class="sxs-lookup"><span data-stu-id="822b3-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="822b3-119">Если клиент не может открыть основное хранилище, он должен открыть дополнительное хранилище и сделать его значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="822b3-120">Обновляет строку таблицы состояния хранилища сообщений, устанавливая флаг STATUS_SECONDARY_STORE в столбце **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="822b3-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="822b3-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="822b3-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="822b3-122">Задает флаг STATUS_SIMPLE_STORE в свойстве **PR_RESOURCE_FLAGS** хранилища сообщений в строке таблицы состояний, в строке таблицы хранилища сообщений и в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="822b3-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="822b3-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="822b3-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="822b3-124">Задает флаг STATUS_SIMPLE_STORE в свойстве **PR_RESOURCE_FLAGS** хранилища сообщений в строке таблицы состояний и строке таблицы хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="822b3-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="822b3-125">Профиль не изменяется.</span><span class="sxs-lookup"><span data-stu-id="822b3-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="822b3-126">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="822b3-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="822b3-127">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="822b3-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="822b3-128">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="822b3-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="822b3-129">возврата Указатель на идентификатор записи хранилища сообщений, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="822b3-130">Если клиент передает значение NULL в _лпентрид_, в качестве значения по умолчанию не выбрано ни одного хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="822b3-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="822b3-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="822b3-131">Return value</span></span>

<span data-ttu-id="822b3-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="822b3-132">S_OK</span></span> 
  
> <span data-ttu-id="822b3-133">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="822b3-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="822b3-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="822b3-134">Remarks</span></span>

<span data-ttu-id="822b3-135">Метод **IMAPISession:: сетдефаултсторе** устанавливает хранилище сообщений одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="822b3-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="822b3-136">Хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="822b3-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="822b3-137">Основной банк сообщений для сеанса.</span><span class="sxs-lookup"><span data-stu-id="822b3-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="822b3-138">Дополнительное хранилище сообщений для сеанса.</span><span class="sxs-lookup"><span data-stu-id="822b3-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="822b3-139">Для установки хранилища сообщений по умолчанию в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) в хранилище сообщений должны быть установлены следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="822b3-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="822b3-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="822b3-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="822b3-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="822b3-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="822b3-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="822b3-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="822b3-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="822b3-143">Notes to callers</span></span>

<span data-ttu-id="822b3-144">Вы можете определить хранилище сообщений по умолчанию для сеанса, изменив таблицу состояния и выполнив поиск значения флага STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="822b3-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="822b3-145">Строка с этим параметром представляет собой хранилище сообщений, назначенное в качестве сеанса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="822b3-146">Если установлен флаг MAPI_DEFAULT_STORE или MAPI_SIMPLE_STORE_PERMANENT, MAPI обновляет данные профиля, таблицы хранилища сообщений и таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="822b3-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="822b3-147">При внесении изменений в параметр хранилища сообщений по умолчанию создаются следующие уведомления:</span><span class="sxs-lookup"><span data-stu-id="822b3-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="822b3-148">Уведомление о событии **фневтаблемодифиед** создается для каждой затронутой строки в таблице "хранилище сообщений" и "состояние".</span><span class="sxs-lookup"><span data-stu-id="822b3-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="822b3-149">В очередь печати MAPI отправляется внутреннее уведомление.</span><span class="sxs-lookup"><span data-stu-id="822b3-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="822b3-150">Выполняемые операции выполняются без изменений; новые операции, использующие хранилище сообщений по умолчанию (например, загрузку сообщений), обрабатываются для нового хранилища по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="822b3-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="822b3-151">MFCMAPI reference</span></span>

<span data-ttu-id="822b3-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="822b3-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="822b3-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="822b3-153">**File**</span></span>|<span data-ttu-id="822b3-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="822b3-154">**Function**</span></span>|<span data-ttu-id="822b3-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="822b3-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="822b3-156">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="822b3-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="822b3-157">Кмаиндлг:: Онсетдефаултсторе</span><span class="sxs-lookup"><span data-stu-id="822b3-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="822b3-158">MFCMAPI использует метод **IMAPISession:: сетдефаултсторе** , чтобы установить выбранное хранилище в качестве хранилища по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="822b3-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="822b3-159">См. также</span><span class="sxs-lookup"><span data-stu-id="822b3-159">See also</span></span>



[<span data-ttu-id="822b3-160">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="822b3-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="822b3-161">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="822b3-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="822b3-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="822b3-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="822b3-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="822b3-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="822b3-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="822b3-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

