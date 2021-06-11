---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419592"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="ecdb0-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="ecdb0-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="ecdb0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecdb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecdb0-105">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ecdb0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ecdb0-106">Parameters</span></span>

 <span data-ttu-id="ecdb0-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ecdb0-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ecdb0-108">[in] Указатель на имя удаляемого профиля.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="ecdb0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ecdb0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ecdb0-110">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ecdb0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecdb0-111">Return value</span></span>

<span data-ttu-id="ecdb0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ecdb0-112">S_OK</span></span> 
  
> <span data-ttu-id="ecdb0-113">Профиль был успешно удален.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="ecdb0-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ecdb0-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ecdb0-115">Указанного профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecdb0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecdb0-116">Remarks</span></span>

<span data-ttu-id="ecdb0-117">Метод **IProfAdmin::D eleteProfile** удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="ecdb0-118">Если удалить профиль используется при призыве **DeleteProfile,** **DeleteProfile** возвращает S_OK, но не удаляет профиль немедленно.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="ecdb0-119">Вместо этого **DeleteProfile** отмечает профиль для удаления и удаляет его после того, как он больше не используется, когда все его активные сеансы закончились.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="ecdb0-120">Функция точки входа для каждой службы сообщений в профиле называется с MSG_SERVICE_DELETE в параметре _ulContext._</span><span class="sxs-lookup"><span data-stu-id="ecdb0-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="ecdb0-121">Сначала функция удаляет службу, а затем удаляет раздел профилей службы.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="ecdb0-122">Функция точки входа службы сообщений не будет снова вызвана после удаления службы.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="ecdb0-123">Для удаления профиля не требуется пароль.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ecdb0-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ecdb0-124">MFCMAPI reference</span></span>

<span data-ttu-id="ecdb0-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ecdb0-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ecdb0-126">**File**</span></span>|<span data-ttu-id="ecdb0-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ecdb0-127">**Function**</span></span>|<span data-ttu-id="ecdb0-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ecdb0-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ecdb0-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ecdb0-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ecdb0-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="ecdb0-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="ecdb0-131">MFCMAPI использует **метод IProfAdmin::D eleteProfile** для удаления выбранного профиля.</span><span class="sxs-lookup"><span data-stu-id="ecdb0-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecdb0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ecdb0-132">See also</span></span>



[<span data-ttu-id="ecdb0-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="ecdb0-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="ecdb0-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="ecdb0-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="ecdb0-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecdb0-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="ecdb0-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ecdb0-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

