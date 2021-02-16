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
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422763"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="c0971-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="c0971-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="c0971-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0971-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0971-105">Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0971-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="c0971-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0971-106">Parameters</span></span>

 <span data-ttu-id="c0971-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c0971-107">_lpUID_</span></span>
  
> <span data-ttu-id="c0971-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений, которая должна администрироваться.</span><span class="sxs-lookup"><span data-stu-id="c0971-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="c0971-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0971-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c0971-110">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="c0971-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="c0971-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="c0971-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="c0971-112">[out] Указатель на указатель на объект администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0971-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0971-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0971-113">Return value</span></span>

<span data-ttu-id="c0971-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0971-114">S_OK</span></span> 
  
> <span data-ttu-id="c0971-115">Объект администрирования поставщика успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="c0971-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="c0971-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c0971-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c0971-117">**MAPIUID, на** который указывает _lpUID,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="c0971-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c0971-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0971-118">Remarks</span></span>

<span data-ttu-id="c0971-119">Метод **IMsgServiceAdmin::AdminProviders** предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0971-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="c0971-120">Администрирование поставщика — это объект, который поддерживает [интерфейс IProviderAdmin](iprovideradminiunknown.md) и позволяет клиентам:</span><span class="sxs-lookup"><span data-stu-id="c0971-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="c0971-121">Добавление поставщиков служб в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="c0971-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="c0971-122">Удаление поставщиков услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c0971-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="c0971-123">Откройте разделы профиля.</span><span class="sxs-lookup"><span data-stu-id="c0971-123">Open profile sections.</span></span>
    
- <span data-ttu-id="c0971-124">Доступ к таблице поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c0971-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="c0971-125">Типы изменений, которые фактически можно внести в службу сообщений во время использования профиля, зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c0971-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="c0971-126">Однако большинство служб сообщений не поддерживают такие изменения, как добавление и удаление поставщиков, пока используется профиль.</span><span class="sxs-lookup"><span data-stu-id="c0971-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0971-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c0971-127">Notes to callers</span></span>

<span data-ttu-id="c0971-128">Чтобы получить структуру **MAPIUID** для службы сообщений для **администрирования,** извлекает столбец свойства PR_SERVICE_UID ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c0971-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="c0971-129">Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="c0971-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c0971-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c0971-130">MFCMAPI reference</span></span>

<span data-ttu-id="c0971-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c0971-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c0971-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c0971-132">**File**</span></span>|<span data-ttu-id="c0971-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c0971-133">**Function**</span></span>|<span data-ttu-id="c0971-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c0971-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0971-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c0971-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="c0971-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="c0971-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="c0971-137">MFCMAPI использует метод **IMsgServiceAdmin::AdminProviders** для открытия объекта администрирования поставщика для службы.</span><span class="sxs-lookup"><span data-stu-id="c0971-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0971-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c0971-138">See also</span></span>



[<span data-ttu-id="c0971-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0971-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="c0971-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c0971-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c0971-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0971-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="c0971-142">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c0971-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

