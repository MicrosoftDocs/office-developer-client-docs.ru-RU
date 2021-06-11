---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422084"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="6c8c7-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="6c8c7-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="6c8c7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c8c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c8c7-105">Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="6c8c7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6c8c7-106">Parameters</span></span>

 <span data-ttu-id="6c8c7-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6c8c7-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6c8c7-108">[in] Указатель на имя измененного профиля.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="6c8c7-109">Параметр  _lpszProfileName_ не должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="6c8c7-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="6c8c7-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="6c8c7-111">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="6c8c7-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6c8c7-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="6c8c7-113">[in] Ручка родительского окна для любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="6c8c7-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c8c7-114">_ulFlags_</span></span>
  
> <span data-ttu-id="6c8c7-115">[in] Немного флагов, которые контролируют ирисовку объекта администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="6c8c7-116">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6c8c7-116">The following flags can be set:</span></span>
    
<span data-ttu-id="6c8c7-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6c8c7-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6c8c7-118">Включает отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="6c8c7-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c8c7-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6c8c7-120">Имя профиля находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="6c8c7-121">Если флаг MAPI_UNICODE не установлен, имя находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="6c8c7-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="6c8c7-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="6c8c7-123">[вышел] Указатель на указатель на объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c8c7-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c8c7-124">Return value</span></span>

<span data-ttu-id="6c8c7-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c8c7-125">S_OK</span></span> 
  
> <span data-ttu-id="6c8c7-126">Объект администрирования службы сообщений был успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="6c8c7-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="6c8c7-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="6c8c7-128">Указанный профиль не существует, или пароль был неправ, и диалоговое окно не могло отображаться пользователю, чтобы запросить правильный пароль, так как MAPI_DIALOG не был задан в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="6c8c7-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6c8c7-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6c8c7-130">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6c8c7-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c8c7-131">Remarks</span></span>

<span data-ttu-id="6c8c7-132">Метод **IProfAdmin::AdminServices** предоставляет доступ к объекту администрирования службы сообщений для внесения изменений конфигурации в службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="6c8c7-133">Параметр  _lpszPassword должен_ быть NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c8c7-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6c8c7-134">Notes to callers</span></span>

<span data-ttu-id="6c8c7-135">Хотя вы можете получить [указатель IMsgServiceAdmin,](imsgserviceadminiunknown.md) позвонив по этому методу или [IMAPISession::AdminServices,](imapisession-adminservices.md)позвоните **по телефону IProfAdmin::AdminServices,** если у вас строго клиент конфигурации и не предлагаются функции обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="6c8c7-136">**IProfAdmin::AdminServices** не создает объект сеанса и не загружает поставщиков услуг, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="6c8c7-137">Вы не можете использовать **IProfAdmin::AdminServices** для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="6c8c7-138">Поэтому необходимо указать существующий допустимый профиль _в lpszProfileName._</span><span class="sxs-lookup"><span data-stu-id="6c8c7-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="6c8c7-139">Если указанного профиля не существует, **IProfAdmin::AdminServices** возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="6c8c7-140">Имя профиля может быть до 64 символов в длину и может включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="6c8c7-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="6c8c7-141">Все буквы, включая символы акцента и символы подчеркнуть.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="6c8c7-142">Встроенные пробелы, но не ведущие и не ведущие.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c8c7-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6c8c7-143">MFCMAPI reference</span></span>

<span data-ttu-id="6c8c7-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c8c7-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6c8c7-145">**File**</span></span>|<span data-ttu-id="6c8c7-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6c8c7-146">**Function**</span></span>|<span data-ttu-id="6c8c7-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6c8c7-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c8c7-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6c8c7-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="6c8c7-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="6c8c7-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="6c8c7-150">MFCMAPI использует метод **IProfAdmin::AdminServices** для открытия объекта администрирования службы сообщений для выбранного профиля для добавления служб.</span><span class="sxs-lookup"><span data-stu-id="6c8c7-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c8c7-151">См. также</span><span class="sxs-lookup"><span data-stu-id="6c8c7-151">See also</span></span>



[<span data-ttu-id="6c8c7-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="6c8c7-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="6c8c7-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c8c7-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="6c8c7-154">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6c8c7-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

