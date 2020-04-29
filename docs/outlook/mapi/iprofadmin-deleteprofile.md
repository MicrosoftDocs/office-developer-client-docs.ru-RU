---
title: ипрофадминделетепрофиле
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
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="d7cad-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="d7cad-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="d7cad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7cad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7cad-105">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="d7cad-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d7cad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7cad-106">Parameters</span></span>

 <span data-ttu-id="d7cad-107">_лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="d7cad-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="d7cad-108">возврата Указатель на имя профиля, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="d7cad-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="d7cad-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7cad-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d7cad-110">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="d7cad-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7cad-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7cad-111">Return value</span></span>

<span data-ttu-id="d7cad-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7cad-112">S_OK</span></span> 
  
> <span data-ttu-id="d7cad-113">Профиль успешно удален.</span><span class="sxs-lookup"><span data-stu-id="d7cad-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="d7cad-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d7cad-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d7cad-115">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="d7cad-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7cad-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7cad-116">Remarks</span></span>

<span data-ttu-id="d7cad-117">Метод **ипрофадмин::D елетепрофиле** удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="d7cad-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="d7cad-118">Если профиль для удаления используется при вызове **делетепрофиле** , **делетепрофиле** возвращает S_OK, но не удаляет его немедленно.</span><span class="sxs-lookup"><span data-stu-id="d7cad-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="d7cad-119">Вместо этого **делетепрофиле** помечает профиль для удаления и удаляет его после того, как он больше не будет использоваться после завершения всех активных сеансов.</span><span class="sxs-lookup"><span data-stu-id="d7cad-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="d7cad-120">Функция точки входа для каждой службы сообщений в профиле вызывается со значением MSG_SERVICE_DELETE, установленным в параметре _улконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="d7cad-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="d7cad-121">Сначала функция удаляет службу, а затем удаляет раздел профиля службы.</span><span class="sxs-lookup"><span data-stu-id="d7cad-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="d7cad-122">Функция точки входа службы сообщений не вызывается повторно после удаления службы.</span><span class="sxs-lookup"><span data-stu-id="d7cad-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="d7cad-123">Для удаления профиля не требуется указывать пароль.</span><span class="sxs-lookup"><span data-stu-id="d7cad-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7cad-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d7cad-124">MFCMAPI reference</span></span>

<span data-ttu-id="d7cad-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d7cad-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7cad-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d7cad-126">**File**</span></span>|<span data-ttu-id="d7cad-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d7cad-127">**Function**</span></span>|<span data-ttu-id="d7cad-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d7cad-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7cad-129">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="d7cad-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d7cad-130">хрремовепрофиле</span><span class="sxs-lookup"><span data-stu-id="d7cad-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="d7cad-131">MFCMAPI использует метод **ипрофадмин::D елетепрофиле** для удаления выбранного профиля.</span><span class="sxs-lookup"><span data-stu-id="d7cad-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7cad-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d7cad-132">See also</span></span>



[<span data-ttu-id="d7cad-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="d7cad-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="d7cad-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="d7cad-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="d7cad-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7cad-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="d7cad-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d7cad-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

