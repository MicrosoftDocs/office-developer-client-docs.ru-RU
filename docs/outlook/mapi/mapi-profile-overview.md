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
# <a name="mapi-profile-overview"></a><span data-ttu-id="c065f-103">Обзор профиля MAPI</span><span class="sxs-lookup"><span data-stu-id="c065f-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="c065f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c065f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c065f-105">Профиль — это набор сведений о службах сообщений и поставщиках услуг, которые будут доступны пользователю клиентского приложения во время определенного сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="c065f-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="c065f-106">У каждого пользователя есть по крайней мере один профиль; Многие пользователи хранят несколько пользователей.</span><span class="sxs-lookup"><span data-stu-id="c065f-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="c065f-107">Например, у пользователя может быть один профиль для работы со службой хранилища сообщений на сервере и другой профиль для работы со службой хранилища сообщений на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c065f-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="c065f-108">Пользователю может потребоваться получить доступ к одному набору систем обмена сообщениями, используя соответствующие транспортные службы для части дня и другой набор для оставшейся части дня.</span><span class="sxs-lookup"><span data-stu-id="c065f-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="c065f-109">Профили предоставляют гибкий способ выбора комбинаций служб системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c065f-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="c065f-110">Профили могут иметь имена длиной до 64 буквенно-цифровых символов.</span><span class="sxs-lookup"><span data-stu-id="c065f-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="c065f-111">Имена могут включать символы ударения, знаки подчеркивания и встроенные пробелы, а также не могут содержать пробелы в начале или конце.</span><span class="sxs-lookup"><span data-stu-id="c065f-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="c065f-112">Профили организованы иерархически и делятся на разделы с одним разделом для каждой службы сообщений и одним разделом для каждого поставщика услуг в службе.</span><span class="sxs-lookup"><span data-stu-id="c065f-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="c065f-113">Связанные разделы связаны, что упрощает навигацию по данным.</span><span class="sxs-lookup"><span data-stu-id="c065f-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="c065f-114">Каждый раздел содержит ряд записей, которые использует MAPI или клиентское приложение для настройки.</span><span class="sxs-lookup"><span data-stu-id="c065f-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="c065f-115">Записи, включенные в профиль, отличаются от службы сообщений до службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c065f-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="c065f-116">Ниже приведены некоторые общие записи.</span><span class="sxs-lookup"><span data-stu-id="c065f-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="c065f-117">Имя каждой службы сообщений или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="c065f-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="c065f-118">Имена библиотек DLL, которые содержат поставщиков услуг и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c065f-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="c065f-119">Имя каждой функции точки входа для каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c065f-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="c065f-120">Список поставщиков услуг, составляющих каждую службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="c065f-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="c065f-121">Профили можно создавать во время установки, когда служба MAPI или служба сообщений загружена на компьютер или позже.</span><span class="sxs-lookup"><span data-stu-id="c065f-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="c065f-122">MAPI предоставляет мастер профилей для администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="c065f-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="c065f-123">Мастер профилей — это приложение, которое создает новые профили с минимальным объемом работы.</span><span class="sxs-lookup"><span data-stu-id="c065f-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="c065f-124">По мере возможности мастер использует значения по умолчанию, что экономит время и усилия пользователей.</span><span class="sxs-lookup"><span data-stu-id="c065f-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="c065f-125">Пользователи вводят значения только в случае крайней необходимости.</span><span class="sxs-lookup"><span data-stu-id="c065f-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="c065f-126">Дополнительные сведения см. в разделе [Создание профиля с помощью мастера профилей](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="c065f-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="c065f-127">Вы также можете использовать центр развертывания Office, чтобы создать новый профиль.</span><span class="sxs-lookup"><span data-stu-id="c065f-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="c065f-128">Дополнительные сведения см. в разделе [Центр развертывания Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="c065f-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c065f-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c065f-129">See also</span></span>



[<span data-ttu-id="c065f-130">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="c065f-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

