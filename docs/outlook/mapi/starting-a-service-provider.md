---
title: Запуск поставщика услуг
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439557"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="12fe3-103">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="12fe3-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="12fe3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12fe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12fe3-105">В определенный момент после того, как клиент начнет сеанс с ПОМОЩЬЮ MAPI, будет запущен ваш поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="12fe3-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="12fe3-106">Поставщики транспорта запущены, когда клиент запрашивает свои службы.</span><span class="sxs-lookup"><span data-stu-id="12fe3-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="12fe3-107">Поставщики адресной книги и магазина сообщений запущены во время процесса работы клиента.</span><span class="sxs-lookup"><span data-stu-id="12fe3-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="12fe3-108">Клиент вызывает [IMAPISession::OpenAddressBook,](imapisession-openaddressbook.md) чтобы загрузить каждого поставщика адресной книги, включенных в профиль и [IMAPISession::OpenMsgStore,](imapisession-openmsgstore.md) для загрузки определенного поставщика хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="12fe3-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="12fe3-109">Поставщики адресных книг, которые являются частью службы сообщений, запущены перед любым из других поставщиков в службе.</span><span class="sxs-lookup"><span data-stu-id="12fe3-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="12fe3-110">MAPI запускает каждого поставщика услуг в активном профиле, выступая следующим образом:</span><span class="sxs-lookup"><span data-stu-id="12fe3-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="12fe3-111">Поиск имени DLL в профиле.</span><span class="sxs-lookup"><span data-stu-id="12fe3-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="12fe3-112">Необходимо зарегистрировать имя DLL поставщика в файле конфигурации Mapisvc.inf, чтобы убедиться, что оно отображается в профиле.</span><span class="sxs-lookup"><span data-stu-id="12fe3-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="12fe3-113">Когда поставщик услуг добавляется в профиль по отдельности или как часть службы сообщений, все разделы **[Поставщик услуг]** из Mapisvc.inf, применимые к поставщику, копируется в профиль.</span><span class="sxs-lookup"><span data-stu-id="12fe3-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="12fe3-114">Дополнительные сведения о структуре Mapisvc.inf см. в формате файла [MapiSvc.inf.](file-format-of-mapisvc-inf.md)</span><span class="sxs-lookup"><span data-stu-id="12fe3-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="12fe3-115">Вызов функции API Windows **LoadLibrary** для загрузки DLL.</span><span class="sxs-lookup"><span data-stu-id="12fe3-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="12fe3-116">Так как MAPI вызывает **LoadLibrary** каждый раз, когда использует DLL поставщика услуг (независимо от того, загружена ли она) или только в первый раз, поставщик услуг не должен делать предположений о том, сколько раз он будет загружен.</span><span class="sxs-lookup"><span data-stu-id="12fe3-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="12fe3-117">Для каждого вызова **LoadLibrary** MAPI совершает вызов функции API Windows **FreeLibrary,** когда DLL поставщика услуг больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="12fe3-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="12fe3-118">Вызов функции точки входа для поставщика.</span><span class="sxs-lookup"><span data-stu-id="12fe3-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="12fe3-119">MAPI вызывает функцию точки входа поставщика для инициации процесса входа.</span><span class="sxs-lookup"><span data-stu-id="12fe3-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="12fe3-120">Функции точки входа гарантируют использование версии интерфейса поставщика услуг (SPI), совместимой с версией, используемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="12fe3-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="12fe3-121">Эти функции также возвращают указатели на вновь созданные объекты поставщика.</span><span class="sxs-lookup"><span data-stu-id="12fe3-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="12fe3-122">Дополнительные сведения о создании функции точки входа для поставщика см. в реализации функции точки [входа поставщика услуг.](implementing-a-service-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="12fe3-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12fe3-123">См. также</span><span class="sxs-lookup"><span data-stu-id="12fe3-123">See also</span></span>



[<span data-ttu-id="12fe3-124">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="12fe3-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

