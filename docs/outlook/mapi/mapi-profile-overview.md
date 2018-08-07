---
title: Обзор профилей MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 573709c4374786bb1bd3d763c8ba91de59f7fb1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809782"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="eca35-103">Обзор профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="eca35-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="eca35-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eca35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eca35-105">Профиль — это набор сведений о службах сообщения и поставщиков услуг, которые пользователь клиентского приложения может быть доступен во время отдельного сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="eca35-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="eca35-106">Каждый пользователь имеет по крайней мере один профиль; число пользователей оставьте несколько.</span><span class="sxs-lookup"><span data-stu-id="eca35-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="eca35-107">Например пользователь может иметь один профиль для работы со службой store сообщения на стороне сервера и другого профиля для работы со службой store сообщения на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="eca35-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="eca35-108">Пользователь может понадобиться доступ к один набор систем обмена сообщениями с помощью служб соответствующие транспорта для части дня и другой набор для остальной части дня.</span><span class="sxs-lookup"><span data-stu-id="eca35-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="eca35-109">Профили обеспечивают гибкие возможности для выбора сочетания служб системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="eca35-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="eca35-110">Профили могут иметь имена до 64 буквенно-цифровых символов в длину.</span><span class="sxs-lookup"><span data-stu-id="eca35-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="eca35-111">Имена может включать диакритических знаков, знак подчеркивания и пробелы и не может содержать начальных и конечных пробелов.</span><span class="sxs-lookup"><span data-stu-id="eca35-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="eca35-112">Профили упорядочить иерархически и разделены на разделы, содержащие один раздел для каждой службы сообщений и один раздел для каждого поставщика служб в службе.</span><span class="sxs-lookup"><span data-stu-id="eca35-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="eca35-113">Связанные разделы связаны, что позволяет просматривать сведения.</span><span class="sxs-lookup"><span data-stu-id="eca35-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="eca35-114">Каждый раздел содержит ряд записей, которые MAPI или клиентское приложение использует для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="eca35-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="eca35-115">Записей, включенных в профиль в зависимости от службы сообщений для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="eca35-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="eca35-116">Ниже приведены некоторые распространенные записей:</span><span class="sxs-lookup"><span data-stu-id="eca35-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="eca35-117">Имя каждой службы сообщений или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="eca35-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="eca35-118">Имя библиотеки DLL, которые содержат поставщиков услуг и сообщений служб.</span><span class="sxs-lookup"><span data-stu-id="eca35-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="eca35-119">Имя функции точки входа для каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="eca35-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="eca35-120">Список поставщиков услуг, входящих в состав каждой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="eca35-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="eca35-121">Можно создавать профили, во время установки, когда загружается MAPI или службы сообщений на компьютер, или в любой момент позже.</span><span class="sxs-lookup"><span data-stu-id="eca35-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="eca35-122">MAPI предоставляет мастер профиля для администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="eca35-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="eca35-123">Мастер профиля — это приложение, которое создает новые профили с минимальный объем работы.</span><span class="sxs-lookup"><span data-stu-id="eca35-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="eca35-124">Мастер использует значения по умолчанию для параметров где это возможно, сохранение пользователей время и силы.</span><span class="sxs-lookup"><span data-stu-id="eca35-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="eca35-125">Пользователи вводят значения только в том случае, когда это абсолютно необходимо.</span><span class="sxs-lookup"><span data-stu-id="eca35-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="eca35-126">Для получения дополнительных сведений см [профиля с помощью мастера профилей](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="eca35-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="eca35-127">Также можно использовать центр развертывания Office для создания нового профиля.</span><span class="sxs-lookup"><span data-stu-id="eca35-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="eca35-128">Дополнительные сведения см в [Центр развертывания Office](http://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="eca35-128">For more information, see [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eca35-129">См. также</span><span class="sxs-lookup"><span data-stu-id="eca35-129">See also</span></span>



[<span data-ttu-id="eca35-130">Функции MAPI и архитектура</span><span class="sxs-lookup"><span data-stu-id="eca35-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

