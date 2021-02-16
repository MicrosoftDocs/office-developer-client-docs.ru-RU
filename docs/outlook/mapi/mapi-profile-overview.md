---
title: Обзор профиля MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328169"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="26398-103">Обзор профиля MAPI</span><span class="sxs-lookup"><span data-stu-id="26398-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="26398-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26398-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26398-105">Профиль — это коллекция сведений о службах сообщений и поставщиках служб, которые пользователь клиентского приложения хочет сделать доступными во время определенного сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="26398-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="26398-106">Каждый пользователь имеет по крайней мере один профиль; многие пользователи могут сохранить несколько.</span><span class="sxs-lookup"><span data-stu-id="26398-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="26398-107">Например, у пользователя может быть один профиль для работы со службой хранения сообщений на сервере, а другой профиль для работы со службой хранения сообщений на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="26398-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="26398-108">Пользователю может потребоваться доступ к одному набору систем обмена сообщениями, используя соответствующие службы транспорта для части дня, а другой набор для остальной части дня.</span><span class="sxs-lookup"><span data-stu-id="26398-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="26398-109">Профили предоставляют гибкий способ выбора комбинаций систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="26398-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="26398-110">Профили могут иметь имена длиной до 64 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="26398-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="26398-111">Имена могут включать знаки элементов, подчеркивание и внедренные пробелы, а также не могут включать пробелы в конце или в конце.</span><span class="sxs-lookup"><span data-stu-id="26398-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="26398-112">Профили организованы по иерархии и разделены на разделы, по одному разделу для каждой службы сообщений и по одному разделу для каждого поставщика службы в службе.</span><span class="sxs-lookup"><span data-stu-id="26398-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="26398-113">Связанные разделы связаны, что упрощает навигацию по информации.</span><span class="sxs-lookup"><span data-stu-id="26398-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="26398-114">Каждый раздел содержит ряд записей, которые MAPI или клиентские приложения используют для настройки.</span><span class="sxs-lookup"><span data-stu-id="26398-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="26398-115">Записи, включенные в профиль, отличаются от службы сообщений к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="26398-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="26398-116">К числу распространенных записей относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="26398-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="26398-117">Имя каждой службы сообщений или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="26398-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="26398-118">Имя DLL, содержащих поставщиков услуг и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="26398-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="26398-119">Имя функции точки входа каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="26398-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="26398-120">Список поставщиков служб, которые составляют каждую службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="26398-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="26398-121">Профили могут создаваться во время установки, при загрузке MAPI или службы сообщений на компьютер или в любое время.</span><span class="sxs-lookup"><span data-stu-id="26398-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="26398-122">MAPI предоставляет мастер профилей для администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="26398-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="26398-123">Мастер профилей — это приложение, которое создает новые профили с минимальным объемом работы.</span><span class="sxs-lookup"><span data-stu-id="26398-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="26398-124">Мастер по возможности использует значения по умолчанию для параметров, экономя время и усилия пользователей.</span><span class="sxs-lookup"><span data-stu-id="26398-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="26398-125">Пользователи вводить значения только при абсолютной необходимости.</span><span class="sxs-lookup"><span data-stu-id="26398-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="26398-126">Дополнительные сведения см. в [теме "Создание профиля с помощью мастера профилей".](creating-a-profile-by-using-the-profile-wizard.md)</span><span class="sxs-lookup"><span data-stu-id="26398-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="26398-127">Для создания нового профиля можно также использовать средство настройки Office.</span><span class="sxs-lookup"><span data-stu-id="26398-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="26398-128">Дополнительные сведения см. в разделе [Центр развертывания Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="26398-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26398-129">См. также</span><span class="sxs-lookup"><span data-stu-id="26398-129">See also</span></span>



[<span data-ttu-id="26398-130">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="26398-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

