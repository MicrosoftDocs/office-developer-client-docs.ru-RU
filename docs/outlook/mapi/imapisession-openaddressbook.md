---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329423"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="aa1fd-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="aa1fd-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="aa1fd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa1fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa1fd-105">Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="aa1fd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="aa1fd-106">Parameters</span></span>

 <span data-ttu-id="aa1fd-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="aa1fd-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="aa1fd-108">[in] Ручка родительского окна общего диалогового окна адресов и других связанных дисплеев.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="aa1fd-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="aa1fd-109">_lpInterface_</span></span>
  
> <span data-ttu-id="aa1fd-110">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="aa1fd-111">Передача **null** возвращает указатель к стандартному интерфейсу адресной [книги, IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="aa1fd-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="aa1fd-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa1fd-112">_ulFlags_</span></span>
  
> <span data-ttu-id="aa1fd-113">[in] Немного флагов, которые контролируют открытие адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="aa1fd-114">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="aa1fd-114">The following flag can be set:</span></span>
    
<span data-ttu-id="aa1fd-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="aa1fd-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="aa1fd-116">Подавляет отображение диалогов.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="aa1fd-117">Если флаг AB_NO_DIALOG не установлен, поставщики адресных книг, которые вносят вклад в интегрированную адресную книгу, могут подсказать пользователю любую необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="aa1fd-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="aa1fd-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="aa1fd-119">[вышел] Указатель на указатель на адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa1fd-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa1fd-120">Return value</span></span>

<span data-ttu-id="aa1fd-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa1fd-121">S_OK</span></span> 
  
> <span data-ttu-id="aa1fd-122">Адресная книга была успешно открыта.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="aa1fd-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="aa1fd-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="aa1fd-124">Вызов удался, но контейнеры одного или более поставщиков адресной книги не удалось открыть.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="aa1fd-125">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="aa1fd-126">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="aa1fd-127">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="aa1fd-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa1fd-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa1fd-128">Remarks</span></span>

<span data-ttu-id="aa1fd-129">Метод **IMAPISession::OpenAddressBook** открывает интегрированную адресную книгу MAPI, коллекцию контейнеров верхнего уровня всех поставщиков адресных книг в профиле.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="aa1fd-130">Указатель, возвращаемый в  _параметре lppAdrBook,_ предоставляет дополнительный доступ к содержимому адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="aa1fd-131">Это позволяет вызываемой службе выполнять такие задачи, как открытие отдельных контейнеров, поиск пользователей сообщений и отображение общих диалогов адресов.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa1fd-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="aa1fd-132">Notes to callers</span></span>

 <span data-ttu-id="aa1fd-133">**OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, если не удается загрузить один или несколько поставщиков адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="aa1fd-134">Это значение является предупреждением, а не значением ошибки; обрабатывать его так, как S_OK.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="aa1fd-135">**OpenAddressBook** всегда возвращает допустимый указатель в  _параметре lppAdrBook_ независимо от того, сколько поставщиков адресной книги не удалось загрузить.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="aa1fd-136">Поэтому перед отключением необходимо всегда вызывать метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="aa1fd-137">Когда **OpenAddressBook** MAPI_W_ERRORS_RETURNED, позвоните [в службу IMAPISession::GetLastError,](imapisession-getlasterror.md) чтобы получить структуру [MAPIERROR,](mapierror.md) которая содержит сведения о поставщиках сбоя.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="aa1fd-138">Возвращается **одна структура MAPIERROR,** которая содержит сведения, предоставленные всеми поставщиками.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa1fd-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aa1fd-139">MFCMAPI reference</span></span>

<span data-ttu-id="aa1fd-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa1fd-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="aa1fd-141">**File**</span></span>|<span data-ttu-id="aa1fd-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="aa1fd-142">**Function**</span></span>|<span data-ttu-id="aa1fd-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="aa1fd-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa1fd-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="aa1fd-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="aa1fd-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="aa1fd-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="aa1fd-146">MFCMAPI использует **метод IMAPISession::OpenAddressBook** для получения интегрированной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aa1fd-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa1fd-147">См. также</span><span class="sxs-lookup"><span data-stu-id="aa1fd-147">See also</span></span>



[<span data-ttu-id="aa1fd-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa1fd-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="aa1fd-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="aa1fd-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="aa1fd-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="aa1fd-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="aa1fd-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa1fd-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="aa1fd-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="aa1fd-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

