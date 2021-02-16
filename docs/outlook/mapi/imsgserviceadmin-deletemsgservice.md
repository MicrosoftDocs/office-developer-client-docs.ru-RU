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
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407384"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="cae2a-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="cae2a-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="cae2a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae2a-105">Удаляет службу сообщений из профиля.</span><span class="sxs-lookup"><span data-stu-id="cae2a-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="cae2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cae2a-106">Parameters</span></span>

 <span data-ttu-id="cae2a-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="cae2a-107">_lpuid_</span></span>
  
> <span data-ttu-id="cae2a-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор удаляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae2a-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cae2a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cae2a-109">Return value</span></span>

<span data-ttu-id="cae2a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="cae2a-110">S_OK</span></span> 
  
> <span data-ttu-id="cae2a-111">Служба сообщений была удалена.</span><span class="sxs-lookup"><span data-stu-id="cae2a-111">The message service was deleted.</span></span>
    
<span data-ttu-id="cae2a-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cae2a-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cae2a-113">**MAPIUID, на** который указывает _lpuid,_ не соответствует существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae2a-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cae2a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cae2a-114">Remarks</span></span>

<span data-ttu-id="cae2a-115">Метод **IMsgServiceAdmin::D eleteMsgService** удаляет службу сообщений из профиля.</span><span class="sxs-lookup"><span data-stu-id="cae2a-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="cae2a-116">**DeleteMsgService** удаляет все разделы профиля, связанные со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae2a-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="cae2a-117">**DeleteMsgService** выполняет следующие действия для удаления службы сообщений:</span><span class="sxs-lookup"><span data-stu-id="cae2a-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="cae2a-118">Вызывает функцию точки входа службы сообщений с параметром  _ulContext MSG_SERVICE_DELETE_ перед удалением разделов профиля.</span><span class="sxs-lookup"><span data-stu-id="cae2a-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="cae2a-119">Это позволяет службе выполнять любые задачи, выполняемые конкретной службой.</span><span class="sxs-lookup"><span data-stu-id="cae2a-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="cae2a-120">Удаляет службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae2a-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="cae2a-121">Удаляет раздел профиля службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae2a-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="cae2a-122">Функция точки входа службы сообщений не будет повторно вызвана после удаления службы.</span><span class="sxs-lookup"><span data-stu-id="cae2a-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cae2a-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cae2a-123">Notes to callers</span></span>

<span data-ttu-id="cae2a-124">Чтобы получить структуру **MAPIUID** для удаляемой службы сообщений, извлеките столбец свойства **PR_SERVICE_UID** ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae2a-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="cae2a-125">Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="cae2a-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cae2a-126">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cae2a-126">MFCMAPI reference</span></span>

<span data-ttu-id="cae2a-127">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cae2a-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cae2a-128">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cae2a-128">**File**</span></span>|<span data-ttu-id="cae2a-129">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cae2a-129">**Function**</span></span>|<span data-ttu-id="cae2a-130">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cae2a-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cae2a-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cae2a-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="cae2a-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="cae2a-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="cae2a-133">MFCMAPI использует метод **IMsgServiceAdmin::D eleteMsgService** для удаления выбранной службы.</span><span class="sxs-lookup"><span data-stu-id="cae2a-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cae2a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="cae2a-134">See also</span></span>



[<span data-ttu-id="cae2a-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cae2a-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cae2a-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cae2a-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="cae2a-137">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cae2a-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

