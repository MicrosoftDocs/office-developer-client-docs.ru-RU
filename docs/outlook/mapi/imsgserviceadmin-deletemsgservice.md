---
title: Имсгсервицеадминделетемсгсервице
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309991"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="7eb98-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="7eb98-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="7eb98-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7eb98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7eb98-105">Удаляет службу сообщений из профиля.</span><span class="sxs-lookup"><span data-stu-id="7eb98-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="7eb98-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7eb98-106">Parameters</span></span>

 <span data-ttu-id="7eb98-107">_лпуид_</span><span class="sxs-lookup"><span data-stu-id="7eb98-107">_lpuid_</span></span>
  
> <span data-ttu-id="7eb98-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор удаляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eb98-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7eb98-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7eb98-109">Return value</span></span>

<span data-ttu-id="7eb98-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7eb98-110">S_OK</span></span> 
  
> <span data-ttu-id="7eb98-111">Служба сообщений удалена.</span><span class="sxs-lookup"><span data-stu-id="7eb98-111">The message service was deleted.</span></span>
    
<span data-ttu-id="7eb98-112">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="7eb98-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7eb98-113">**Мапиуид** , на который указывает _лпуид_ , не отвечает существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eb98-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7eb98-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7eb98-114">Remarks</span></span>

<span data-ttu-id="7eb98-115">Метод **имсгсервицеадмин::D елетемсгсервице** Удаляет службу сообщений из профиля.</span><span class="sxs-lookup"><span data-stu-id="7eb98-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="7eb98-116">**Делетемсгсервице** удаляет все разделы профиля, связанные со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eb98-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="7eb98-117">**Делетемсгсервице** выполняет следующие действия, чтобы удалить службу сообщений:</span><span class="sxs-lookup"><span data-stu-id="7eb98-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="7eb98-118">Вызывает функцию точки входа службы сообщений с параметром _улконтекст_ , РАВНым мсг_сервице_делете, перед удалением разделов профиля.</span><span class="sxs-lookup"><span data-stu-id="7eb98-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="7eb98-119">Это позволяет службе выполнять любые задачи, связанные с определенной службой.</span><span class="sxs-lookup"><span data-stu-id="7eb98-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="7eb98-120">Удаляет службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eb98-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="7eb98-121">Удаляет раздел профиля службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eb98-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="7eb98-122">Функция точки входа службы сообщений не вызывается повторно после удаления службы.</span><span class="sxs-lookup"><span data-stu-id="7eb98-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7eb98-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7eb98-123">Notes to callers</span></span>

<span data-ttu-id="7eb98-124">Чтобы получить структуру **мапиуид** для службы сообщений, которую необходимо удалить, извлеките столбец свойства **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из строки службы сообщений в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eb98-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="7eb98-125">Для получения дополнительных сведений обратитесь к процедуре, описанной в методе [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7eb98-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7eb98-126">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7eb98-126">MFCMAPI reference</span></span>

<span data-ttu-id="7eb98-127">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7eb98-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7eb98-128">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7eb98-128">**File**</span></span>|<span data-ttu-id="7eb98-129">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7eb98-129">**Function**</span></span>|<span data-ttu-id="7eb98-130">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7eb98-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7eb98-131">Мсгсервицетабледлг. cpp</span><span class="sxs-lookup"><span data-stu-id="7eb98-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="7eb98-132">Кмсгсервицетабледлг:: Онделетеселектедитем</span><span class="sxs-lookup"><span data-stu-id="7eb98-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="7eb98-133">MFCMAPI использует метод **имсгсервицеадмин::D елетемсгсервице** , чтобы удалить выбранную службу.</span><span class="sxs-lookup"><span data-stu-id="7eb98-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7eb98-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7eb98-134">See also</span></span>



[<span data-ttu-id="7eb98-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7eb98-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7eb98-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7eb98-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="7eb98-137">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7eb98-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

