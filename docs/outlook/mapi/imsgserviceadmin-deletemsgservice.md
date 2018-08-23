---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571145"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="cadc9-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="cadc9-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="cadc9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cadc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cadc9-105">Удаление службы сообщений из профиля.</span><span class="sxs-lookup"><span data-stu-id="cadc9-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="cadc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cadc9-106">Parameters</span></span>

 <span data-ttu-id="cadc9-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="cadc9-107">_lpuid_</span></span>
  
> <span data-ttu-id="cadc9-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для удаления.</span><span class="sxs-lookup"><span data-stu-id="cadc9-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cadc9-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cadc9-109">Return value</span></span>

<span data-ttu-id="cadc9-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cadc9-110">S_OK</span></span> 
  
> <span data-ttu-id="cadc9-111">Служба сообщений был удален.</span><span class="sxs-lookup"><span data-stu-id="cadc9-111">The message service was deleted.</span></span>
    
<span data-ttu-id="cadc9-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cadc9-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cadc9-113">**MAPIUID** , на который указывает _lpuid_ не соответствует существующую службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="cadc9-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cadc9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="cadc9-114">Remarks</span></span>

<span data-ttu-id="cadc9-115">Метод **IMsgServiceAdmin::DeleteMsgService** удаляет службы сообщений из профиля.</span><span class="sxs-lookup"><span data-stu-id="cadc9-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="cadc9-116">**DeleteMsgService** удаляет все разделы профилей, связанные со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="cadc9-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="cadc9-117">**DeleteMsgService** выполняет следующие действия, чтобы удалить службы сообщений:</span><span class="sxs-lookup"><span data-stu-id="cadc9-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="cadc9-118">Вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_DELETE перед удалением раздела профилей.</span><span class="sxs-lookup"><span data-stu-id="cadc9-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="cadc9-119">Это позволяет службы для выполнения задач, используемых службой.</span><span class="sxs-lookup"><span data-stu-id="cadc9-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="cadc9-120">Удаляет службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="cadc9-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="cadc9-121">Удаление раздела профиля службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="cadc9-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="cadc9-122">После удаления службы функцию точки входа службы сообщений не вызывает еще раз.</span><span class="sxs-lookup"><span data-stu-id="cadc9-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cadc9-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cadc9-123">Notes to callers</span></span>

<span data-ttu-id="cadc9-124">Для получения **MAPIUID** структуры для службы сообщений для удаления, получить столбец свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="cadc9-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="cadc9-125">Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="cadc9-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cadc9-126">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="cadc9-126">MFCMAPI reference</span></span>

<span data-ttu-id="cadc9-127">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="cadc9-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cadc9-128">**����**</span><span class="sxs-lookup"><span data-stu-id="cadc9-128">**File**</span></span>|<span data-ttu-id="cadc9-129">**�������**</span><span class="sxs-lookup"><span data-stu-id="cadc9-129">**Function**</span></span>|<span data-ttu-id="cadc9-130">**�����������**</span><span class="sxs-lookup"><span data-stu-id="cadc9-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cadc9-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cadc9-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="cadc9-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="cadc9-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="cadc9-133">Mfcmapi (en) метод **IMsgServiceAdmin::DeleteMsgService** используется для удаления выбранного службы.</span><span class="sxs-lookup"><span data-stu-id="cadc9-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cadc9-134">См. также</span><span class="sxs-lookup"><span data-stu-id="cadc9-134">See also</span></span>



[<span data-ttu-id="cadc9-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cadc9-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cadc9-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cadc9-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="cadc9-137">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cadc9-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

