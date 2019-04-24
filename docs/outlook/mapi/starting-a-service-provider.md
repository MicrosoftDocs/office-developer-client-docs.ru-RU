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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341715"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="aeb86-103">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="aeb86-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="aeb86-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aeb86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aeb86-105">В некоторый момент после того, как клиент начнет сеанс с MAPI, ваш поставщик услуг будет запущен.</span><span class="sxs-lookup"><span data-stu-id="aeb86-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="aeb86-106">Поставщики транспорта запускаются, когда клиент отправляет запрос на их службы.</span><span class="sxs-lookup"><span data-stu-id="aeb86-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="aeb86-107">Адресные книги и поставщики хранилища сообщений запускаются в процессе входа клиента.</span><span class="sxs-lookup"><span data-stu-id="aeb86-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="aeb86-108">Клиент вызывает [IMAPISession:: опенаддрессбук](imapisession-openaddressbook.md) для загрузки каждого из поставщиков адресных книг, включенных в профиль, и [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) для загрузки определенного поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="aeb86-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="aeb86-109">Поставщики адресных книг, являющиеся частью службы сообщений, запускаются до других поставщиков в службе.</span><span class="sxs-lookup"><span data-stu-id="aeb86-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="aeb86-110">MAPI запускает каждого поставщика услуг в активном профиле, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="aeb86-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="aeb86-111">Поиск имени DLL в профиле.</span><span class="sxs-lookup"><span data-stu-id="aeb86-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="aeb86-112">Необходимо зарегистрировать имя библиотеки DLL поставщика в файле конфигурации Mapisvc. INF, чтобы убедиться в том, что он отображается в профиле.</span><span class="sxs-lookup"><span data-stu-id="aeb86-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="aeb86-113">Когда поставщик услуг добавляется в профиль отдельно или в составе службы сообщений, все разделы **[поставщик услуг]** из Mapisvc. INF, применимые к поставщику, копируются в профиль.</span><span class="sxs-lookup"><span data-stu-id="aeb86-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="aeb86-114">Дополнительные сведения о структуре Mapisvc. INF приведены в разделе [Формат файлов файла Mapisvc. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="aeb86-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="aeb86-115">Вызов функции **LOADLIBRARY** API Windows для загрузки DLL.</span><span class="sxs-lookup"><span data-stu-id="aeb86-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="aeb86-116">Так как функция **LoadLibrary вызывает LoadLibrary** всякий раз, когда она использует библиотеку DLL поставщика услуг (независимо от того, была ли она загружена) или только первый раз, поставщик услуг не должен делать предположения о количестве загруженности.</span><span class="sxs-lookup"><span data-stu-id="aeb86-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="aeb86-117">При каждом вызове метода **LoadLibrary**MAPI вызывает функцию Windows API **FREELIBRARY** , если библиотека DLL поставщика услуг больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="aeb86-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="aeb86-118">Вызов функции точки входа для поставщика.</span><span class="sxs-lookup"><span data-stu-id="aeb86-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="aeb86-119">MAPI вызывает функцию точки входа поставщика для запуска процесса входа.</span><span class="sxs-lookup"><span data-stu-id="aeb86-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="aeb86-120">Функции точки входа гарантируют, что вы используете версию интерфейса поставщика услуг (SPI), совместимую с версией, используемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="aeb86-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="aeb86-121">Эти функции также возвращают указатели на вновь созданные объекты поставщика.</span><span class="sxs-lookup"><span data-stu-id="aeb86-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="aeb86-122">Для получения дополнительных сведений о создании функции точки входа для поставщика, ознакомьтесь со статьей [Реализация функции точки входа поставщика услуг](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="aeb86-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aeb86-123">См. также</span><span class="sxs-lookup"><span data-stu-id="aeb86-123">See also</span></span>



[<span data-ttu-id="aeb86-124">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="aeb86-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

