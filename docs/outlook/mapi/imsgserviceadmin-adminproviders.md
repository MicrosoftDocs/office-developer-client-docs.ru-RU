---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1b03245d7af4c6fb3879e597d8345e5d9888e164
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567211"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="92a8b-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="92a8b-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="92a8b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92a8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92a8b-105">Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="92a8b-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="92a8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92a8b-106">Parameters</span></span>

 <span data-ttu-id="92a8b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="92a8b-107">_lpUID_</span></span>
  
> <span data-ttu-id="92a8b-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для администрирования.</span><span class="sxs-lookup"><span data-stu-id="92a8b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="92a8b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="92a8b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="92a8b-110">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="92a8b-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="92a8b-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="92a8b-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="92a8b-112">[out] Указатель на указатель на объект администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="92a8b-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92a8b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92a8b-113">Return value</span></span>

<span data-ttu-id="92a8b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="92a8b-114">S_OK</span></span> 
  
> <span data-ttu-id="92a8b-115">Объект администрирования поставщика успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="92a8b-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="92a8b-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="92a8b-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="92a8b-117">**MAPIUID** , на который указывает _lpUID_ не существует.</span><span class="sxs-lookup"><span data-stu-id="92a8b-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="92a8b-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="92a8b-118">Remarks</span></span>

<span data-ttu-id="92a8b-119">Метод **IMsgServiceAdmin::AdminProviders** предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="92a8b-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="92a8b-120">Администрирование поставщика — это объект, который поддерживает интерфейс [IProviderAdmin](iprovideradminiunknown.md) и позволяет клиентам для выполнения следующих:</span><span class="sxs-lookup"><span data-stu-id="92a8b-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="92a8b-121">Добавьте поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="92a8b-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="92a8b-122">Удаление поставщиков услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="92a8b-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="92a8b-123">Откройте разделы профилей.</span><span class="sxs-lookup"><span data-stu-id="92a8b-123">Open profile sections.</span></span>
    
- <span data-ttu-id="92a8b-124">Доступ к таблице поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="92a8b-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="92a8b-125">Типы изменений, которые могут производится службы сообщений во время профиля зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="92a8b-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="92a8b-126">Большинство служб сообщения не поддерживают изменения, такие как добавление и удаление поставщиков во время профиля.</span><span class="sxs-lookup"><span data-stu-id="92a8b-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="92a8b-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="92a8b-127">Notes to callers</span></span>

<span data-ttu-id="92a8b-128">Для получения **MAPIUID** структуры для службы сообщений на администрирование, получение столбца свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="92a8b-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="92a8b-129">Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="92a8b-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="92a8b-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="92a8b-130">MFCMAPI reference</span></span>

<span data-ttu-id="92a8b-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="92a8b-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="92a8b-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="92a8b-132">**File**</span></span>|<span data-ttu-id="92a8b-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="92a8b-133">**Function**</span></span>|<span data-ttu-id="92a8b-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="92a8b-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92a8b-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="92a8b-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="92a8b-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="92a8b-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="92a8b-137">Mfcmapi (en) использует метод **IMsgServiceAdmin::AdminProviders** для открытия объект администрирования поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="92a8b-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92a8b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="92a8b-138">See also</span></span>



[<span data-ttu-id="92a8b-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92a8b-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="92a8b-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="92a8b-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="92a8b-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92a8b-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="92a8b-142">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="92a8b-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

