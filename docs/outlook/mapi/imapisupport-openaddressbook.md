---
title: имаписуппортопенаддрессбук
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
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416883"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="86c41-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="86c41-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="86c41-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86c41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86c41-105">Предоставляет доступ к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="86c41-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="86c41-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86c41-106">Parameters</span></span>

 <span data-ttu-id="86c41-107">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="86c41-107">_lpInterface_</span></span>
  
> <span data-ttu-id="86c41-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="86c41-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="86c41-109">Допустимые значения: NULL, указывающие на стандартную адресную книгу [IAddrBook](iaddrbookimapiprop.md)и IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="86c41-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="86c41-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="86c41-110">_ulFlags_</span></span>
  
> <span data-ttu-id="86c41-111">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="86c41-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="86c41-112">_лппадрбук_</span><span class="sxs-lookup"><span data-stu-id="86c41-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="86c41-113">вышли Указатель на указатель на адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="86c41-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86c41-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86c41-114">Return value</span></span>

<span data-ttu-id="86c41-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="86c41-115">S_OK</span></span> 
  
> <span data-ttu-id="86c41-116">Предоставлен доступ к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="86c41-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="86c41-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="86c41-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="86c41-118">Вызов выполнен успешно, но не удалось загрузить одного или нескольких поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="86c41-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="86c41-119">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="86c41-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="86c41-120">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="86c41-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="86c41-121">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="86c41-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86c41-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="86c41-122">Remarks</span></span>

<span data-ttu-id="86c41-123">Метод **имаписуппорт:: опенаддрессбук** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="86c41-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="86c41-124">Поставщики услуг, обычно тесно связанные с хранилищем сообщений и поставщиками транспорта, вызывают **опенаддрессбук** , чтобы получить доступ к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="86c41-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="86c41-125">Возвращенный указатель **IAddrBook** можно использовать для различных задач адресной книги, включая открытие контейнеров адресных книг, Поиск пользователей обмена сообщениями и отображение диалоговых окон адресов.</span><span class="sxs-lookup"><span data-stu-id="86c41-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="86c41-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="86c41-126">Notes to callers</span></span>

 <span data-ttu-id="86c41-127">**Опенаддрессбук** могут возвращать MAPI_W_ERRORS_RETURNED, если не удается загрузить одного или нескольких поставщиков адресной книги в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="86c41-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="86c41-128">Это значение является предупреждением, и вы должны считать вызов успешным.</span><span class="sxs-lookup"><span data-stu-id="86c41-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="86c41-129">Даже если не удалось загрузить все поставщики адресных книг, **опенаддрессбук** по-прежнему завершается успешно, возвращается MAPI_W_ERRORS_RETURNED и указатель **IAddrBook** в параметре _лппадрбук_ .</span><span class="sxs-lookup"><span data-stu-id="86c41-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="86c41-130">Так как **опенаддрессбук** всегда возвращает допустимый указатель **IAddrBook** , его необходимо освободить после завершения использования.</span><span class="sxs-lookup"><span data-stu-id="86c41-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="86c41-131">Если одному или нескольким поставщикам адресных книг не удалось загрузить, вызовите метод [имаписуппорт:: GetLastError](imapisupport-getlasterror.md) , чтобы получить структуру [мапиеррор](mapierror.md) , содержащую сведения о незагруженных поставщиках.</span><span class="sxs-lookup"><span data-stu-id="86c41-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86c41-132">См. также</span><span class="sxs-lookup"><span data-stu-id="86c41-132">See also</span></span>



[<span data-ttu-id="86c41-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="86c41-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="86c41-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="86c41-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="86c41-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="86c41-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

