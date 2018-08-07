---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809151"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="72339-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="72339-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="72339-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72339-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72339-105">Предоставляет доступ к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="72339-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="72339-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72339-106">Parameters</span></span>

 <span data-ttu-id="72339-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="72339-107">_lpInterface_</span></span>
  
> <span data-ttu-id="72339-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="72339-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="72339-109">Допустимые значения: NULL, которое указывает стандартный адресной книги интерфейс [IAddrBook](iaddrbookimapiprop.md)и IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="72339-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="72339-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72339-110">_ulFlags_</span></span>
  
> <span data-ttu-id="72339-111">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="72339-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="72339-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="72339-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="72339-113">[out] Указатель на указатель в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="72339-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72339-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="72339-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="72339-115">S_OK</span></span> 
  
> <span data-ttu-id="72339-116">Был предоставлен доступ к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="72339-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="72339-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="72339-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="72339-118">Вызов завершился успешно, но не удалось загрузить один или несколько поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="72339-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="72339-119">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="72339-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="72339-120">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="72339-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="72339-121">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="72339-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72339-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="72339-122">Remarks</span></span>

<span data-ttu-id="72339-123">Метод **IMAPISupport::OpenAddressBook** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="72339-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="72339-124">Поставщики услуг, обычно тесно связанных сообщений хранилища и поставщиками транспорта, вызовите **OpenAddressBook** , чтобы получить доступ к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="72339-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="72339-125">Возвращенный указатель **IAddrBook** можно использовать для различных задач адресной книги, включая Открытие адресной книги контейнеров, поиск пользователей обмена мгновенными сообщениями и отображение диалоговых окон адрес.</span><span class="sxs-lookup"><span data-stu-id="72339-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="72339-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="72339-126">Notes to callers</span></span>

 <span data-ttu-id="72339-127">**OpenAddressBook** может вернуть MAPI_W_ERRORS_RETURNED, если не удается загрузить один или несколько поставщиками адресной книги в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="72339-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="72339-128">Это значение — предупреждения и вызова следует рассматривать как успешно.</span><span class="sxs-lookup"><span data-stu-id="72339-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="72339-129">Даже в том случае, если все поставщиками адресной книги не удалось загрузить, **OpenAddressBook** по-прежнему завершается успешно, возвращая MAPI_W_ERRORS_RETURNED и указатель **IAddrBook** с помощью параметра _lppAdrBook_ .</span><span class="sxs-lookup"><span data-stu-id="72339-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="72339-130">Так как **OpenAddressBook** всегда возвращает указатель на допустимый **IAddrBook** , необходимо удалить после завершения с помощью его.</span><span class="sxs-lookup"><span data-stu-id="72339-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="72339-131">Если не удалось загрузить один или несколько поставщиками адресной книги, вызовите [IMAPISupport::GetLastError](imapisupport-getlasterror.md) для получения [MAPIERROR](mapierror.md) структура, содержащая сведения о поставщиках, которые не были загружены.</span><span class="sxs-lookup"><span data-stu-id="72339-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72339-132">См. также</span><span class="sxs-lookup"><span data-stu-id="72339-132">See also</span></span>



[<span data-ttu-id="72339-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="72339-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="72339-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="72339-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="72339-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="72339-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

