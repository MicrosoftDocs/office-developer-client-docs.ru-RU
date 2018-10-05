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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396976"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="82aa9-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="82aa9-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="82aa9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82aa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82aa9-105">Открывает интегрированной адресной книги MAPI, возвращает указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="82aa9-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="82aa9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82aa9-106">Parameters</span></span>

 <span data-ttu-id="82aa9-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="82aa9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="82aa9-108">[in] Дескриптор родительского окна стандартным диалоговым окном адрес и других, связанных с отображает.</span><span class="sxs-lookup"><span data-stu-id="82aa9-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="82aa9-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="82aa9-109">_lpInterface_</span></span>
  
> <span data-ttu-id="82aa9-110">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="82aa9-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="82aa9-111">Передача **значения null** возвращает указатель на стандартный интерфейс в адресной книге, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="82aa9-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="82aa9-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82aa9-112">_ulFlags_</span></span>
  
> <span data-ttu-id="82aa9-113">[in] Битовая маска флаги, который определяет открывающий адресной книги.</span><span class="sxs-lookup"><span data-stu-id="82aa9-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="82aa9-114">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="82aa9-114">The following flag can be set:</span></span>
    
<span data-ttu-id="82aa9-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="82aa9-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="82aa9-116">Запрещает отображение диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="82aa9-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="82aa9-117">Если флаг AB_NO_DIALOG не установлен, поставщиками адресных книг, которые используются в интегрированной адресной книги может запрашивать у пользователя все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="82aa9-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="82aa9-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="82aa9-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="82aa9-119">[out] Указатель на указатель в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="82aa9-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82aa9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82aa9-120">Return value</span></span>

<span data-ttu-id="82aa9-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="82aa9-121">S_OK</span></span> 
  
> <span data-ttu-id="82aa9-122">В адресной книге, был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="82aa9-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="82aa9-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="82aa9-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="82aa9-124">Вызов завершился успешно, но не удается открыть контейнеров один или несколько поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="82aa9-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="82aa9-125">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="82aa9-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="82aa9-126">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="82aa9-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="82aa9-127">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="82aa9-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82aa9-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="82aa9-128">Remarks</span></span>

<span data-ttu-id="82aa9-129">Метод **IMAPISession::OpenAddressBook** открывает интегрированной адресной книги MAPI, семейства сайтов верхнего уровня контейнеров всех поставщиками адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="82aa9-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="82aa9-130">Указатель, который возвращается в параметре _lppAdrBook_ дальнейшей предоставляет доступ к содержимому в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="82aa9-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="82aa9-131">Это позволяет для выполнения задач, таких как открывающий отдельными контейнеры, обмена мгновенными сообщениями пользователи поиск и отображение общие диалоговые окна адрес звонящего.</span><span class="sxs-lookup"><span data-stu-id="82aa9-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82aa9-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="82aa9-132">Notes to callers</span></span>

 <span data-ttu-id="82aa9-133">**OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, если не удается загрузить один или несколько поставщиками адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="82aa9-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="82aa9-134">Это значение — это предупреждение не значением ошибки; обработать его как значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="82aa9-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="82aa9-135">**OpenAddressBook** всегда возвращает указатель на допустимый в параметре _lppAdrBook_ , независимо от того, сколько поставщиками адресной книги не удалось загрузить.</span><span class="sxs-lookup"><span data-stu-id="82aa9-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="82aa9-136">Таким образом всегда вызовите метод [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) адресной книги к определенному моменту перед выходом из системы.</span><span class="sxs-lookup"><span data-stu-id="82aa9-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="82aa9-137">При **OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, вызовите [IMAPISession::GetLastError](imapisession-getlasterror.md) для получения [MAPIERROR](mapierror.md) структура, содержащая сведения о поставщиках со сбоями.</span><span class="sxs-lookup"><span data-stu-id="82aa9-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="82aa9-138">Возвращается один **MAPIERROR** структуры, которая содержит сведения, предоставленные всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="82aa9-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="82aa9-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="82aa9-139">MFCMAPI reference</span></span>

<span data-ttu-id="82aa9-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="82aa9-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="82aa9-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="82aa9-141">**File**</span></span>|<span data-ttu-id="82aa9-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="82aa9-142">**Function**</span></span>|<span data-ttu-id="82aa9-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="82aa9-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82aa9-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="82aa9-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="82aa9-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="82aa9-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="82aa9-146">Mfcmapi (en) использует метод **IMAPISession::OpenAddressBook** для получения интегрированной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="82aa9-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82aa9-147">См. также</span><span class="sxs-lookup"><span data-stu-id="82aa9-147">See also</span></span>



[<span data-ttu-id="82aa9-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="82aa9-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="82aa9-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="82aa9-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="82aa9-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="82aa9-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="82aa9-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="82aa9-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="82aa9-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="82aa9-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

