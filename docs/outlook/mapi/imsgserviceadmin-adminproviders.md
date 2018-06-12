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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809351"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="5434a-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="5434a-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="5434a-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5434a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5434a-105">Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="5434a-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="5434a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5434a-106">Parameters</span></span>

 <span data-ttu-id="5434a-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5434a-107">_lpUID_</span></span>
  
> <span data-ttu-id="5434a-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для администрирования.</span><span class="sxs-lookup"><span data-stu-id="5434a-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="5434a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5434a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5434a-110">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="5434a-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="5434a-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="5434a-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="5434a-112">[out] Указатель на указатель на объект администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="5434a-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5434a-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5434a-113">Return value</span></span>

<span data-ttu-id="5434a-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5434a-114">S_OK</span></span> 
  
> <span data-ttu-id="5434a-115">Объект администрирования поставщика успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="5434a-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="5434a-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5434a-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5434a-117">**MAPIUID** , на который указывает _lpUID_ не существует.</span><span class="sxs-lookup"><span data-stu-id="5434a-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5434a-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="5434a-118">Remarks</span></span>

<span data-ttu-id="5434a-119">Метод **IMsgServiceAdmin::AdminProviders** предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="5434a-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="5434a-120">Администрирование поставщика — это объект, который поддерживает интерфейс [IProviderAdmin](iprovideradminiunknown.md) и позволяет клиентам для выполнения следующих:</span><span class="sxs-lookup"><span data-stu-id="5434a-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="5434a-121">Добавьте поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5434a-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="5434a-122">Удаление поставщиков услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5434a-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="5434a-123">Откройте разделы профилей.</span><span class="sxs-lookup"><span data-stu-id="5434a-123">Open profile sections.</span></span>
    
- <span data-ttu-id="5434a-124">Доступ к таблице поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5434a-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="5434a-125">Типы изменений, которые могут производится службы сообщений во время профиля зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5434a-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="5434a-126">Большинство служб сообщения не поддерживают изменения, такие как добавление и удаление поставщиков во время профиля.</span><span class="sxs-lookup"><span data-stu-id="5434a-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5434a-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5434a-127">Notes to callers</span></span>

<span data-ttu-id="5434a-128">Для получения **MAPIUID** структуры для службы сообщений на администрирование, получение столбца свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5434a-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="5434a-129">Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5434a-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5434a-130">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="5434a-130">MFCMAPI reference</span></span>

<span data-ttu-id="5434a-131">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="5434a-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5434a-132">**����**</span><span class="sxs-lookup"><span data-stu-id="5434a-132">**File**</span></span>|<span data-ttu-id="5434a-133">**�������**</span><span class="sxs-lookup"><span data-stu-id="5434a-133">**Function**</span></span>|<span data-ttu-id="5434a-134">**�����������**</span><span class="sxs-lookup"><span data-stu-id="5434a-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5434a-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5434a-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="5434a-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="5434a-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="5434a-137">Mfcmapi (en) использует метод **IMsgServiceAdmin::AdminProviders** для открытия объект администрирования поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="5434a-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5434a-138">См. также</span><span class="sxs-lookup"><span data-stu-id="5434a-138">See also</span></span>



[<span data-ttu-id="5434a-139">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5434a-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="5434a-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5434a-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5434a-141">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5434a-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="5434a-142">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5434a-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

