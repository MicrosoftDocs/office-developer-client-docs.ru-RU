---
title: Ипрофадминадминсервицес
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309599"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="4924d-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="4924d-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="4924d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4924d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4924d-105">Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="4924d-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="4924d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4924d-106">Parameters</span></span>

 <span data-ttu-id="4924d-107">_Лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="4924d-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="4924d-108">возврата Указатель на имя профиля, который требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="4924d-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="4924d-109">Параметр _лпсзпрофиленаме_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4924d-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="4924d-110">_Лпсзпассворд_</span><span class="sxs-lookup"><span data-stu-id="4924d-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="4924d-111">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4924d-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="4924d-112">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="4924d-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="4924d-113">возврата Дескриптор родительского окна для всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="4924d-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="4924d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4924d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="4924d-115">возврата Битовая маска флагов, которые управляют извлечением объекта администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="4924d-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="4924d-116">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4924d-116">The following flags can be set:</span></span>
    
<span data-ttu-id="4924d-117">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4924d-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4924d-118">Включает отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4924d-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="4924d-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4924d-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4924d-120">Имя профиля имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="4924d-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="4924d-121">Если флаг МАПИ_УНИКОДЕ не установлен, имя указывается в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4924d-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="4924d-122">_Лппсервицеадмин_</span><span class="sxs-lookup"><span data-stu-id="4924d-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="4924d-123">вышли Указатель на указатель на объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="4924d-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4924d-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4924d-124">Return value</span></span>

<span data-ttu-id="4924d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="4924d-125">S_OK</span></span> 
  
> <span data-ttu-id="4924d-126">Объект администрирования службы сообщений успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="4924d-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="4924d-127">МАПИ_Е_ЛОГОН_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="4924d-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="4924d-128">Указанный профиль не существует или неправильный пароль, и пользователю не удалось отобразить диалоговое окно, чтобы запросить правильный пароль, так как МАПИ_ДИАЛОГ не был задан в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="4924d-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="4924d-129">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="4924d-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4924d-130">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4924d-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4924d-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="4924d-131">Remarks</span></span>

<span data-ttu-id="4924d-132">Метод **ипрофадмин:: админсервицес** предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в конфигурацию служб сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="4924d-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="4924d-133">Параметр _лпсзпассворд_ должен иметь значение null или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="4924d-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4924d-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4924d-134">Notes to callers</span></span>

<span data-ttu-id="4924d-135">Несмотря на то, что вы можете получить указатель [имсгсервицеадмин](imsgserviceadminiunknown.md) , вызвав либо этот метод, либо [IMAPISession:: Админсервицес](imapisession-adminservices.md), Call **ипрофадмин:: админсервицес** , если у вас есть строго клиент конфигурации и не предоставляет возможности обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4924d-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="4924d-136">**Ипрофадмин:: админсервицес** не создает объект Session и не загружает поставщиков служб, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="4924d-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="4924d-137">Вы не можете использовать **ипрофадмин:: админсервицес** , чтобы создать профиль.</span><span class="sxs-lookup"><span data-stu-id="4924d-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="4924d-138">Поэтому необходимо указать существующий допустимый профиль в _лпсзпрофиленаме_.</span><span class="sxs-lookup"><span data-stu-id="4924d-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="4924d-139">Если указанный профиль не существует, **ипрофадмин:: админсервицес** возвращает мапи_е_логон_фаилед.</span><span class="sxs-lookup"><span data-stu-id="4924d-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="4924d-140">Длина имени профиля может доставлять до 64 символов и может включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="4924d-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="4924d-141">Все буквенно-цифровые символы, включая диакритические знаки и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="4924d-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="4924d-142">Внутренние пробелы, но не ведущие и замыкающие пробелы.</span><span class="sxs-lookup"><span data-stu-id="4924d-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="4924d-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4924d-143">MFCMAPI reference</span></span>

<span data-ttu-id="4924d-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4924d-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4924d-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="4924d-145">**File**</span></span>|<span data-ttu-id="4924d-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="4924d-146">**Function**</span></span>|<span data-ttu-id="4924d-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="4924d-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4924d-148">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="4924d-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="4924d-149">Храддсервицетопрофиле</span><span class="sxs-lookup"><span data-stu-id="4924d-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="4924d-150">MFCMAPI использует метод **ипрофадмин:: админсервицес** , чтобы открыть объект администрирования службы сообщений для выбранного профиля, чтобы добавить службы.</span><span class="sxs-lookup"><span data-stu-id="4924d-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4924d-151">См. также</span><span class="sxs-lookup"><span data-stu-id="4924d-151">See also</span></span>



[<span data-ttu-id="4924d-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="4924d-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="4924d-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4924d-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="4924d-154">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="4924d-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

