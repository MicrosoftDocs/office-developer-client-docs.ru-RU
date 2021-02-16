---
title: Реализация функции точки входа поставщика адресной книги
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
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="3a6b4-103">Реализация функции точки входа поставщика адресной книги</span><span class="sxs-lookup"><span data-stu-id="3a6b4-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="3a6b4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a6b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a6b4-105">Когда клиентские приложения вызывает [MAPILogonEx](mapilogonex.md) для начала сеанса с использованием профиля, содержашего поставщика адресной книги, MAPI загружает поставщика и всех остальных, которые являются частью профиля.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="3a6b4-106">MAPI узнает об имени функции точки входа поставщика, изучив профиль.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="3a6b4-107">Помните, что эта функция не то же самое, что функция точки входа DLL; см. документацию **по DllMain** в документации win32.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="3a6b4-108">Существует несколько записей, некоторые из которых должны отображаться в файле конфигурации mapisvc.inf, которые включены в раздел профиля каждого поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="3a6b4-109">В следующей таблице перечислены эти записи раздела профиля, а также их необходимо включить в файл mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="3a6b4-110">**Запись раздела профиля**</span><span class="sxs-lookup"><span data-stu-id="3a6b4-110">**Profile section entry**</span></span>|<span data-ttu-id="3a6b4-111">**Требование mapisvc.inf**</span><span class="sxs-lookup"><span data-stu-id="3a6b4-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a6b4-112">PR_DISPLAY_NAME= _строка_</span><span class="sxs-lookup"><span data-stu-id="3a6b4-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="3a6b4-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="3a6b4-113">Optional</span></span>  <br/> |
|<span data-ttu-id="3a6b4-114">PR_PROVIDER_DISPLAY= _string_</span><span class="sxs-lookup"><span data-stu-id="3a6b4-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="3a6b4-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="3a6b4-115">Required</span></span>  <br/> |
|<span data-ttu-id="3a6b4-116">PR_PROVIDER_DLL_NAME= _имя файла DLL_</span><span class="sxs-lookup"><span data-stu-id="3a6b4-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="3a6b4-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="3a6b4-117">Required</span></span>  <br/> |
|<span data-ttu-id="3a6b4-118">PR_RESOURCE_TYPE= _long_</span><span class="sxs-lookup"><span data-stu-id="3a6b4-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="3a6b4-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="3a6b4-119">Required</span></span>  <br/> |
|<span data-ttu-id="3a6b4-120">PR_RESOURCE_FLAGS= _битоваяmask_</span><span class="sxs-lookup"><span data-stu-id="3a6b4-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="3a6b4-121">Необязательна</span><span class="sxs-lookup"><span data-stu-id="3a6b4-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="3a6b4-122">Поставщик адресной книги может напрямую разместить эти сведения в профиле, вызывая метод [IMAPIProp::SetProps](imapiprop-setprops.md) его раздела профиля или косвенно, изменяя MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="3a6b4-123">Профили построены с использованием соответствующей информации в MAPISVC. INF для выбранных поставщиков услуг или служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="3a6b4-124">Дополнительные сведения об организации и содержимом MAPISVC. INF, [см. формат файла MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="3a6b4-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="3a6b4-125">Имя функции точки входа DLL поставщика адресной книги должно быть [ABProviderInit](abproviderinit.md) и соответствовать прототипу **ABProviderInit.**</span><span class="sxs-lookup"><span data-stu-id="3a6b4-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="3a6b4-126">Выполните следующие задачи в функции точки входа DLL поставщика:</span><span class="sxs-lookup"><span data-stu-id="3a6b4-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="3a6b4-127">Проверьте версию интерфейса поставщика услуг (SPI), чтобы убедиться, что MAPI использует версию, совместимую с версией, используемой поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="3a6b4-128">Instantiate an address book provider object.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="3a6b4-129">Не вызывай **MAPIInitialize** или **MAPIUninitialize в** этой функции.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="3a6b4-130">Функция точки входа DLL возвращает объект поставщика и возвращает MAPI указатель на этот объект.</span><span class="sxs-lookup"><span data-stu-id="3a6b4-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

