---
title: Реализация функции точки входа поставщика адресных книг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409715"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="7ce2e-103">Реализация функции точки входа поставщика адресных книг</span><span class="sxs-lookup"><span data-stu-id="7ce2e-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="7ce2e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ce2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ce2e-105">Когда клиентская заявка вызывает [MAPILogonEx](mapilogonex.md) для начала сеанса с помощью профиля, содержашего поставщика адресной книги, MAPI загружает поставщика и всех других пользователей, которые являются частью профиля.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="7ce2e-106">MAPI узнает имя функции точки входа поставщика, посмотрев в профиле.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="7ce2e-107">Помните, что эта функция не такая, как функция точки входа DLL; см. документацию **для DllMain в** документации Win32.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="7ce2e-108">Существует несколько записей, некоторые из которых должны отображаться в файле конфигурации mapisvc.inf, которые включены в раздел профилей каждого поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="7ce2e-109">В следующей таблице перечислены эти записи раздела профилей и должны ли они включаться в файл mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="7ce2e-110">**Запись раздела "Профиль"**</span><span class="sxs-lookup"><span data-stu-id="7ce2e-110">**Profile section entry**</span></span>|<span data-ttu-id="7ce2e-111">**требование mapisvc.inf**</span><span class="sxs-lookup"><span data-stu-id="7ce2e-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ce2e-112">PR_DISPLAY_NAME= _строка_</span><span class="sxs-lookup"><span data-stu-id="7ce2e-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="7ce2e-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7ce2e-113">Optional</span></span>  <br/> |
|<span data-ttu-id="7ce2e-114">PR_PROVIDER_DISPLAY= _строка_</span><span class="sxs-lookup"><span data-stu-id="7ce2e-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="7ce2e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ce2e-115">Required</span></span>  <br/> |
|<span data-ttu-id="7ce2e-116">PR_PROVIDER_DLL_NAME= _имя файла DLL_</span><span class="sxs-lookup"><span data-stu-id="7ce2e-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="7ce2e-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ce2e-117">Required</span></span>  <br/> |
|<span data-ttu-id="7ce2e-118">PR_RESOURCE_TYPE= _длинный_</span><span class="sxs-lookup"><span data-stu-id="7ce2e-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="7ce2e-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ce2e-119">Required</span></span>  <br/> |
|<span data-ttu-id="7ce2e-120">PR_RESOURCE_FLAGS= _bitmask_</span><span class="sxs-lookup"><span data-stu-id="7ce2e-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="7ce2e-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7ce2e-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="7ce2e-122">Поставщик адресной книги может непосредственно разместить эти сведения в профиле, позвонив в метод [IMAPIProp::SetProps](imapiprop-setprops.md) или косвенно, изменяя MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="7ce2e-123">Профили строятся с использованием соответствующих сведений в MAPISVC. INF для выбранных поставщиков или служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="7ce2e-124">Дополнительные сведения об организации и содержимом MAPISVC. INF, [см. формат файла MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="7ce2e-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="7ce2e-125">Имя функции точки входа поставщика адресной книги должно быть [ABProviderInit](abproviderinit.md) и соответствовать прототипу **ABProviderInit.**</span><span class="sxs-lookup"><span data-stu-id="7ce2e-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="7ce2e-126">Выполните следующие задачи в функции точки входа DLL поставщика:</span><span class="sxs-lookup"><span data-stu-id="7ce2e-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="7ce2e-127">Проверьте версию интерфейса поставщика услуг (SPI), чтобы убедиться, что MAPI использует версию, совместимую с версией, которую использует поставщик адресных книг.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="7ce2e-128">Мгновенный доступ к объекту поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="7ce2e-129">Не вызывай **MAPIInitialize или** **MAPIUninitialize в** этой функции.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="7ce2e-130">Функция точки входа DLL мгновенно передает объект поставщика и возвращает в MAPI указатель на этот объект.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

