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
ms.openlocfilehash: aa3c010eafeba7908498965bc0491c993a4a9120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572091"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="85160-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="85160-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="85160-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85160-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85160-105">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="85160-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="85160-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85160-106">Parameters</span></span>

 <span data-ttu-id="85160-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="85160-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="85160-108">[in] Указатель на имя профиля, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="85160-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="85160-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85160-109">_ulFlags_</span></span>
  
> <span data-ttu-id="85160-110">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="85160-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85160-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85160-111">Return value</span></span>

<span data-ttu-id="85160-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="85160-112">S_OK</span></span> 
  
> <span data-ttu-id="85160-113">Профиль успешно удален.</span><span class="sxs-lookup"><span data-stu-id="85160-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="85160-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="85160-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="85160-115">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="85160-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85160-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="85160-116">Remarks</span></span>

<span data-ttu-id="85160-117">Метод **IProfAdmin::DeleteProfile** удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="85160-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="85160-118">Если профиль для удаления используется при вызове **DeleteProfile** , **DeleteProfile** возвращает значение S_OK, но не удаляет профиль немедленно.</span><span class="sxs-lookup"><span data-stu-id="85160-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="85160-119">Вместо этого **DeleteProfile** помечает профиля для удаления и удаляется после его больше не используется, по окончании всех активных сеансов.</span><span class="sxs-lookup"><span data-stu-id="85160-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="85160-120">С MSG_SERVICE_DELETE значение, установленное в параметре _ulContext_ вызывает функцию точки входа для каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="85160-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="85160-121">Во-первых функция удаляет службу, а затем его удаляет раздел службы профилей.</span><span class="sxs-lookup"><span data-stu-id="85160-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="85160-122">После удаления службы функцию точки входа службы сообщений не вызывает еще раз.</span><span class="sxs-lookup"><span data-stu-id="85160-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="85160-123">Чтобы удалить профиль необходим не пароль.</span><span class="sxs-lookup"><span data-stu-id="85160-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="85160-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="85160-124">MFCMAPI reference</span></span>

<span data-ttu-id="85160-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="85160-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="85160-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="85160-126">**File**</span></span>|<span data-ttu-id="85160-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="85160-127">**Function**</span></span>|<span data-ttu-id="85160-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="85160-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="85160-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="85160-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="85160-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="85160-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="85160-131">Mfcmapi (en) метод **IProfAdmin::DeleteProfile** используется для удаления выбранного профиля.</span><span class="sxs-lookup"><span data-stu-id="85160-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85160-132">См. также</span><span class="sxs-lookup"><span data-stu-id="85160-132">See also</span></span>



[<span data-ttu-id="85160-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="85160-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="85160-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="85160-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="85160-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85160-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="85160-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="85160-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

