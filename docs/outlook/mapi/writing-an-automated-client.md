---
title: Написание автоматизированного клиента
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325594"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="a548d-103">Написание автоматизированного клиента</span><span class="sxs-lookup"><span data-stu-id="a548d-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="a548d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a548d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a548d-105">Автоматизированное клиентское приложение — это приложение, которое выполняется в автоматическом режиме без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a548d-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="a548d-106">По умолчанию многие методы интерфейса MAPI демонстрируют пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a548d-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="a548d-107">Все эти методы имеют флаги, позволяющие клиенту разрешить или запретить это отображение.</span><span class="sxs-lookup"><span data-stu-id="a548d-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="a548d-108">Несмотря на то, что служба MAPI ожидает, что эти флаги поддерживаются поставщиками, существует несколько поставщиков, которые не всегда удовлетворяют этим ожиданиям.</span><span class="sxs-lookup"><span data-stu-id="a548d-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="a548d-109">Допустимая причина отсутствия флагов — зависимость от поставщика услуг в другой службе, которая не допускает запрета пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a548d-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="a548d-110">При разработке автоматизированного клиента следует уделять особое внимание используемым поставщикам услуг и способам их настройки.</span><span class="sxs-lookup"><span data-stu-id="a548d-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="a548d-111">Не следует предполагать, что все звонки, поблокирующие пользовательский интерфейс, будут успешными.</span><span class="sxs-lookup"><span data-stu-id="a548d-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="a548d-112">Для автоматизированных клиентов должна быть доступна необходимая информация для правильной настройки каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="a548d-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="a548d-113">Существует два способа предоставления сведений о конфигурации во время входа:</span><span class="sxs-lookup"><span data-stu-id="a548d-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="a548d-114">Поставщик услуг может получить сведения из профиля.</span><span class="sxs-lookup"><span data-stu-id="a548d-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="a548d-115">Поставщик услуг может запросить сведения у пользователя.</span><span class="sxs-lookup"><span data-stu-id="a548d-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="a548d-116">Так как второй параметр недоступен для автоматических клиентов, эти клиенты должны использовать первый параметр.</span><span class="sxs-lookup"><span data-stu-id="a548d-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="a548d-117">Клиенты должны тщательно настраивать их профили, чтобы убедиться, что этот вариант всегда работает.</span><span class="sxs-lookup"><span data-stu-id="a548d-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="a548d-118">Для запуска сеанса MAPI в автоматизированных клиентах всегда устанавливается флаг МАПИ_НО_МАИЛ в вызове функции [мапилогонекс](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="a548d-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

