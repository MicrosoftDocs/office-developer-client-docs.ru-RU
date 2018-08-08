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
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809521"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="6932d-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="6932d-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="6932d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6932d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6932d-105">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="6932d-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6932d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6932d-106">Parameters</span></span>

 <span data-ttu-id="6932d-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6932d-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6932d-108">[in] Указатель на имя профиля, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="6932d-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="6932d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6932d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6932d-110">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="6932d-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6932d-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6932d-111">Return value</span></span>

<span data-ttu-id="6932d-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6932d-112">S_OK</span></span> 
  
> <span data-ttu-id="6932d-113">Профиль успешно удален.</span><span class="sxs-lookup"><span data-stu-id="6932d-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="6932d-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6932d-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6932d-115">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="6932d-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6932d-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="6932d-116">Remarks</span></span>

<span data-ttu-id="6932d-117">Метод **IProfAdmin::DeleteProfile** удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="6932d-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="6932d-118">Если профиль для удаления используется при вызове **DeleteProfile** , **DeleteProfile** возвращает значение S_OK, но не удаляет профиль немедленно.</span><span class="sxs-lookup"><span data-stu-id="6932d-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="6932d-119">Вместо этого **DeleteProfile** помечает профиля для удаления и удаляется после его больше не используется, по окончании всех активных сеансов.</span><span class="sxs-lookup"><span data-stu-id="6932d-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="6932d-120">С MSG_SERVICE_DELETE значение, установленное в параметре _ulContext_ вызывает функцию точки входа для каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="6932d-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="6932d-121">Во-первых функция удаляет службу, а затем его удаляет раздел службы профилей.</span><span class="sxs-lookup"><span data-stu-id="6932d-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="6932d-122">После удаления службы функцию точки входа службы сообщений не вызывает еще раз.</span><span class="sxs-lookup"><span data-stu-id="6932d-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="6932d-123">Чтобы удалить профиль необходим не пароль.</span><span class="sxs-lookup"><span data-stu-id="6932d-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6932d-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="6932d-124">MFCMAPI reference</span></span>

<span data-ttu-id="6932d-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="6932d-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6932d-126">**����**</span><span class="sxs-lookup"><span data-stu-id="6932d-126">**File**</span></span>|<span data-ttu-id="6932d-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="6932d-127">**Function**</span></span>|<span data-ttu-id="6932d-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="6932d-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6932d-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6932d-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6932d-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="6932d-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="6932d-131">Mfcmapi (en) метод **IProfAdmin::DeleteProfile** используется для удаления выбранного профиля.</span><span class="sxs-lookup"><span data-stu-id="6932d-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6932d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6932d-132">See also</span></span>



[<span data-ttu-id="6932d-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="6932d-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="6932d-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="6932d-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="6932d-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6932d-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="6932d-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6932d-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

