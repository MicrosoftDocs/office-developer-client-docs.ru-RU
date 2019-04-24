---
title: Ипрофадминделетепрофиле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309564"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="0c12a-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="0c12a-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="0c12a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c12a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c12a-105">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="0c12a-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0c12a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c12a-106">Parameters</span></span>

 <span data-ttu-id="0c12a-107">_Лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="0c12a-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="0c12a-108">возврата Указатель на имя профиля, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="0c12a-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="0c12a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c12a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0c12a-110">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="0c12a-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c12a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c12a-111">Return value</span></span>

<span data-ttu-id="0c12a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c12a-112">S_OK</span></span> 
  
> <span data-ttu-id="0c12a-113">Профиль успешно удален.</span><span class="sxs-lookup"><span data-stu-id="0c12a-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="0c12a-114">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="0c12a-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0c12a-115">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="0c12a-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c12a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0c12a-116">Remarks</span></span>

<span data-ttu-id="0c12a-117">Метод **ипрофадмин::D елетепрофиле** удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="0c12a-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="0c12a-118">Если профиль, который требуется удалить, используется при вызове **делетепрофиле** , **ДЕЛЕТЕПРОФИЛЕ** возвращает значение S_OK, но не удаляет профиль немедленно.</span><span class="sxs-lookup"><span data-stu-id="0c12a-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="0c12a-119">Вместо этого **делетепрофиле** помечает профиль для удаления и удаляет его после того, как он больше не будет использоваться после завершения всех активных сеансов.</span><span class="sxs-lookup"><span data-stu-id="0c12a-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="0c12a-120">Функция точки входа для каждой службы сообщений в профиле вызывается со значением МСГ_СЕРВИЦЕ_ДЕЛЕТЕ, установленным в параметре _улконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="0c12a-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="0c12a-121">Сначала функция удаляет службу, а затем удаляет раздел профиля службы.</span><span class="sxs-lookup"><span data-stu-id="0c12a-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="0c12a-122">Функция точки входа службы сообщений не вызывается повторно после удаления службы.</span><span class="sxs-lookup"><span data-stu-id="0c12a-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="0c12a-123">Для удаления профиля не требуется указывать пароль.</span><span class="sxs-lookup"><span data-stu-id="0c12a-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0c12a-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0c12a-124">MFCMAPI reference</span></span>

<span data-ttu-id="0c12a-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0c12a-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0c12a-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0c12a-126">**File**</span></span>|<span data-ttu-id="0c12a-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0c12a-127">**Function**</span></span>|<span data-ttu-id="0c12a-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0c12a-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c12a-129">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="0c12a-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0c12a-130">Хрремовепрофиле</span><span class="sxs-lookup"><span data-stu-id="0c12a-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="0c12a-131">MFCMAPI использует метод **ипрофадмин::D елетепрофиле** для удаления выбранного профиля.</span><span class="sxs-lookup"><span data-stu-id="0c12a-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c12a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0c12a-132">See also</span></span>



[<span data-ttu-id="0c12a-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="0c12a-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="0c12a-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="0c12a-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="0c12a-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c12a-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="0c12a-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0c12a-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

