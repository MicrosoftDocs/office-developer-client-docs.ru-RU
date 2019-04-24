---
title: Реализация функции точки входа для поставщика адресных книг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332804"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="b32ae-103">Реализация функции точки входа для поставщика адресных книг</span><span class="sxs-lookup"><span data-stu-id="b32ae-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="b32ae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b32ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b32ae-105">Когда клиентское приложение вызывает [мапилогонекс](mapilogonex.md) для запуска сеанса с использованием профиля, содержащего поставщика адресных книг, MAPI загружает поставщика и все остальные, которые являются частью профиля.</span><span class="sxs-lookup"><span data-stu-id="b32ae-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="b32ae-106">Сведения о имени функции точки входа поставщика MAPI просматриваются в профиле.</span><span class="sxs-lookup"><span data-stu-id="b32ae-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="b32ae-107">Помните, что эта функция отличается от функции точки входа DLL; в документации по Win32 вы найдете документацию по функции **DllMain** .</span><span class="sxs-lookup"><span data-stu-id="b32ae-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="b32ae-108">Существует несколько записей, некоторые из которых должны присутствовать в файле конфигурации Mapisvc. INF, которые включены в раздел profile каждого поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="b32ae-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="b32ae-109">В следующей таблице перечислены эти записи разделов профиля, а также указывается, следует ли включать файл Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="b32ae-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="b32ae-110">**Запись раздела профиля**</span><span class="sxs-lookup"><span data-stu-id="b32ae-110">**Profile section entry**</span></span>|<span data-ttu-id="b32ae-111">**требование к Mapisvc. INF**</span><span class="sxs-lookup"><span data-stu-id="b32ae-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b32ae-112">ПР_ДИСПЛАЙ_НАМЕ = _строка_</span><span class="sxs-lookup"><span data-stu-id="b32ae-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="b32ae-113">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="b32ae-113">Optional</span></span>  <br/> |
|<span data-ttu-id="b32ae-114">ПР_ПРОВИДЕР_ДИСПЛАЙ = _строка_</span><span class="sxs-lookup"><span data-stu-id="b32ae-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="b32ae-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b32ae-115">Required</span></span>  <br/> |
|<span data-ttu-id="b32ae-116">ПР_ПРОВИДЕР_ДЛЛ_НАМЕ = _имя файла DLL_</span><span class="sxs-lookup"><span data-stu-id="b32ae-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="b32ae-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b32ae-117">Required</span></span>  <br/> |
|<span data-ttu-id="b32ae-118">ПР_РЕСАУРЦЕ_ТИПЕ = _Long_</span><span class="sxs-lookup"><span data-stu-id="b32ae-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="b32ae-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b32ae-119">Required</span></span>  <br/> |
|<span data-ttu-id="b32ae-120">ПР_РЕСАУРЦЕ_ФЛАГС = _Битовая маска_</span><span class="sxs-lookup"><span data-stu-id="b32ae-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="b32ae-121">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="b32ae-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="b32ae-122">Поставщик адресных книг может поместить эту информацию в профиль напрямую, вызвав метод [IMAPIProp:: SetProps](imapiprop-setprops.md) в разделе profile или опосредованно, изменив Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="b32ae-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="b32ae-123">Профили создаются с использованием соответствующих сведений в MAPISVC. INF для выбранных поставщиков услуг или служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="b32ae-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="b32ae-124">Для получения дополнительных сведений об организации и содержимом MAPISVC. INF-файла см. в разделе [Формат файла MapiSvc. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="b32ae-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="b32ae-125">Имя функции точки входа DLL поставщика адресных книг должно быть [абпровидеринит](abproviderinit.md) и должно соответствовать прототипу **абпровидеринит** .</span><span class="sxs-lookup"><span data-stu-id="b32ae-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="b32ae-126">Выполните следующие задачи в функции точки входа DLL поставщика:</span><span class="sxs-lookup"><span data-stu-id="b32ae-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="b32ae-127">Проверьте версию интерфейса поставщика услуг (SPI), чтобы убедиться, что протокол MAPI использует версию, совместимую с версией, используемой поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b32ae-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="b32ae-128">Создание экземпляра объекта поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="b32ae-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="b32ae-129">Не вызывайте ни **мапиинитиализе** , ни **мапиунинитиализе** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="b32ae-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="b32ae-130">Функция точки входа DLL создает экземпляр объекта поставщика и возвращается в MAPI указателем на этот объект.</span><span class="sxs-lookup"><span data-stu-id="b32ae-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

