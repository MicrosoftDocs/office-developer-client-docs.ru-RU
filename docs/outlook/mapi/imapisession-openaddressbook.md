---
title: имаписессионопенаддрессбук
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
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="a155f-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="a155f-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="a155f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a155f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a155f-105">Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для получения доступа.</span><span class="sxs-lookup"><span data-stu-id="a155f-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="a155f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a155f-106">Parameters</span></span>

 <span data-ttu-id="a155f-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="a155f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a155f-108">возврата Дескриптор родительского окна для диалогового окна общего адреса и других связанных дисплеев.</span><span class="sxs-lookup"><span data-stu-id="a155f-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="a155f-109">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="a155f-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a155f-110">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="a155f-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="a155f-111">При передаче **значения NULL** возвращается указатель на стандартный интерфейс адресной книги [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a155f-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="a155f-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a155f-112">_ulFlags_</span></span>
  
> <span data-ttu-id="a155f-113">возврата Битовая маска флагов, управляющих открытием адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a155f-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="a155f-114">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a155f-114">The following flag can be set:</span></span>
    
<span data-ttu-id="a155f-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a155f-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="a155f-116">Подавляет отображение диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="a155f-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="a155f-117">Если флаг AB_NO_DIALOG не установлен, то поставщики адресных книг, которые вносят вклад в интегрированную адресную книгу, могут запрашивать у пользователя необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="a155f-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="a155f-118">_лппадрбук_</span><span class="sxs-lookup"><span data-stu-id="a155f-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="a155f-119">вышли Указатель на указатель на адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="a155f-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a155f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a155f-120">Return value</span></span>

<span data-ttu-id="a155f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a155f-121">S_OK</span></span> 
  
> <span data-ttu-id="a155f-122">Адресная книга успешно открыта.</span><span class="sxs-lookup"><span data-stu-id="a155f-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="a155f-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a155f-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a155f-124">Вызов выполнен успешно, но не удается открыть контейнеры одного или нескольких поставщиков адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a155f-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="a155f-125">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="a155f-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a155f-126">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="a155f-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a155f-127">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a155f-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a155f-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="a155f-128">Remarks</span></span>

<span data-ttu-id="a155f-129">Метод **IMAPISession:: опенаддрессбук** открывает интегрированную адресную книгу MAPI, коллекцию контейнеров верхнего уровня для всех поставщиков адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="a155f-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="a155f-130">Указатель, возвращенный в параметре _лппадрбук_ , предоставляет дополнительный доступ к содержимому адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a155f-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="a155f-131">Это позволяет вызывающему абоненту выполнять такие задачи, как открытие отдельных контейнеров, Поиск пользователей обмена сообщениями и отображение общих диалоговых окон адресов.</span><span class="sxs-lookup"><span data-stu-id="a155f-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a155f-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a155f-132">Notes to callers</span></span>

 <span data-ttu-id="a155f-133">**Опенаддрессбук** возвращает MAPI_W_ERRORS_RETURNED, если не удается загрузить одного или нескольких поставщиков адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="a155f-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="a155f-134">Это значение является предупреждением, а не значением ошибки; Обработайте ее так же, как S_OK.</span><span class="sxs-lookup"><span data-stu-id="a155f-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="a155f-135">**Опенаддрессбук** всегда возвращает допустимый указатель в параметре _лппадрбук_ , независимо от того, сколько поставщиков адресной книги не удалось загрузить.</span><span class="sxs-lookup"><span data-stu-id="a155f-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="a155f-136">Таким образом, перед выходом из системы необходимо всегда вызывать метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) адресной книги в некоторый момент.</span><span class="sxs-lookup"><span data-stu-id="a155f-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="a155f-137">Когда **опенаддрессбук** возвращает MAPI_W_ERRORS_RETURNED, вызовите [IMAPISession:: GetLastError](imapisession-getlasterror.md) , чтобы получить структуру [мапиеррор](mapierror.md) , содержащую сведения о неисправном поставщике.</span><span class="sxs-lookup"><span data-stu-id="a155f-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="a155f-138">Возвращается одна структура **мапиеррор** , содержащая сведения, предоставленные всеми поставщиками.</span><span class="sxs-lookup"><span data-stu-id="a155f-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a155f-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a155f-139">MFCMAPI reference</span></span>

<span data-ttu-id="a155f-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a155f-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a155f-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a155f-141">**File**</span></span>|<span data-ttu-id="a155f-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a155f-142">**Function**</span></span>|<span data-ttu-id="a155f-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a155f-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a155f-144">Мапиобжектс. cpp</span><span class="sxs-lookup"><span data-stu-id="a155f-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="a155f-145">Кмапиобжектс:: Жетаддрбук</span><span class="sxs-lookup"><span data-stu-id="a155f-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="a155f-146">MFCMAPI использует метод **IMAPISession:: опенаддрессбук** для получения интегрированной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a155f-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a155f-147">См. также</span><span class="sxs-lookup"><span data-stu-id="a155f-147">See also</span></span>



[<span data-ttu-id="a155f-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a155f-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="a155f-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a155f-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="a155f-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a155f-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a155f-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a155f-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a155f-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a155f-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

