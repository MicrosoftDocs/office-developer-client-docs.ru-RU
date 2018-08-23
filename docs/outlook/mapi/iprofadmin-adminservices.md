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
ms.openlocfilehash: a9e596ff8561d5aabc71ffe3540efaeef8f5b83d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593986"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="53ae1-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="53ae1-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="53ae1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53ae1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53ae1-105">Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="53ae1-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="53ae1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53ae1-106">Parameters</span></span>

 <span data-ttu-id="53ae1-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="53ae1-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="53ae1-108">[in] Указатель на имя профиля, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="53ae1-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="53ae1-109">Параметр _lpszProfileName_ не должна быть NULL.</span><span class="sxs-lookup"><span data-stu-id="53ae1-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="53ae1-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="53ae1-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="53ae1-111">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="53ae1-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="53ae1-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="53ae1-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="53ae1-113">[in] Дескриптор родительского окна для любого диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="53ae1-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="53ae1-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53ae1-114">_ulFlags_</span></span>
  
> <span data-ttu-id="53ae1-115">[in] Битовая маска флаги, который управляет извлечения объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="53ae1-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="53ae1-116">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="53ae1-116">The following flags can be set:</span></span>
    
<span data-ttu-id="53ae1-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="53ae1-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="53ae1-118">Включение отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="53ae1-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="53ae1-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53ae1-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="53ae1-120">Имя профиля — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="53ae1-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="53ae1-121">Если флаг MAPI_UNICODE не установлен, — это имя в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="53ae1-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="53ae1-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="53ae1-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="53ae1-123">[out] Указатель на указатель на объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="53ae1-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53ae1-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="53ae1-124">Return value</span></span>

<span data-ttu-id="53ae1-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="53ae1-125">S_OK</span></span> 
  
> <span data-ttu-id="53ae1-126">Объект администрирования службы сообщение успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="53ae1-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="53ae1-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="53ae1-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="53ae1-128">Указанный профиль не существует, или пароль был неверный и диалоговое окно "" не удается отобразить для пользователя, чтобы запросить правильный пароль, так как MAPI_DIALOG не установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="53ae1-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="53ae1-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="53ae1-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="53ae1-130">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="53ae1-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="53ae1-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="53ae1-131">Remarks</span></span>

<span data-ttu-id="53ae1-132">Метод **IProfAdmin::AdminServices** предоставляет доступ к объекту администрирования службы сообщений для изменения конфигурации службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="53ae1-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="53ae1-133">Параметр _lpszPassword_ должен быть NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="53ae1-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53ae1-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="53ae1-134">Notes to callers</span></span>

<span data-ttu-id="53ae1-135">Несмотря на то, что указатель [IMsgServiceAdmin](imsgserviceadminiunknown.md) можно получить путем вызова метода или в этом [IMAPISession::AdminServices](imapisession-adminservices.md), вызовите **IProfAdmin::AdminServices** , если у пользователя имеется строго конфигурации клиента и предлагают нет функции обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="53ae1-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="53ae1-136">**IProfAdmin::AdminServices** не создается объект сеанса и не загружать никаких поставщиков услуг которого повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="53ae1-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="53ae1-137">**IProfAdmin::AdminServices** нельзя использовать для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="53ae1-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="53ae1-138">Таким образом необходимо указать допустимое существующего профиля в _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="53ae1-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="53ae1-139">Если указанный профиль не существует, **IProfAdmin::AdminServices** возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="53ae1-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="53ae1-140">Имя профиля может быть длиной до 64 символов и может содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="53ae1-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="53ae1-141">Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="53ae1-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="53ae1-142">Пробелы, но не начальных и конечных пробелов.</span><span class="sxs-lookup"><span data-stu-id="53ae1-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="53ae1-143">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="53ae1-143">MFCMAPI reference</span></span>

<span data-ttu-id="53ae1-144">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="53ae1-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53ae1-145">**����**</span><span class="sxs-lookup"><span data-stu-id="53ae1-145">**File**</span></span>|<span data-ttu-id="53ae1-146">**�������**</span><span class="sxs-lookup"><span data-stu-id="53ae1-146">**Function**</span></span>|<span data-ttu-id="53ae1-147">**�����������**</span><span class="sxs-lookup"><span data-stu-id="53ae1-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53ae1-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="53ae1-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="53ae1-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="53ae1-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="53ae1-150">Mfcmapi (en) использует метод **IProfAdmin::AdminServices** для открытия объект сообщения службы администрирования для выбранного профиля для добавления служб.</span><span class="sxs-lookup"><span data-stu-id="53ae1-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53ae1-151">См. также</span><span class="sxs-lookup"><span data-stu-id="53ae1-151">See also</span></span>



[<span data-ttu-id="53ae1-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="53ae1-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="53ae1-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53ae1-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="53ae1-154">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="53ae1-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

