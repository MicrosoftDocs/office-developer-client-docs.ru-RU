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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439767"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="fc247-103">Написание автоматизированного клиента</span><span class="sxs-lookup"><span data-stu-id="fc247-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="fc247-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc247-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc247-105">Автоматическое клиентские приложения — это приложение, которое запускается автоматически и не отображает пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fc247-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="fc247-106">По умолчанию во многих методах интерфейса MAPI имеется пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fc247-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="fc247-107">Все эти методы имеют флаги, которые позволяют клиенту разрешить или подавить этот дисплей.</span><span class="sxs-lookup"><span data-stu-id="fc247-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="fc247-108">Хотя MAPI ожидает, что поставщики услуг будут соблюдать эти флаги, некоторые поставщики не всегда соответствуют этим ожиданиям.</span><span class="sxs-lookup"><span data-stu-id="fc247-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="fc247-109">Допустимой причиной невыполнения флагов является зависимость поставщика службы от другой службы, которая не разрешает подавления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fc247-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="fc247-110">При разработке автоматизированного клиента обратите особое внимание на поставщиков услуг, которые вы используете, и их настройку.</span><span class="sxs-lookup"><span data-stu-id="fc247-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="fc247-111">Не следует предполагать, что все ваши вызовы для подавления пользовательского интерфейса будут успешными.</span><span class="sxs-lookup"><span data-stu-id="fc247-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="fc247-112">Автоматические клиенты должны иметь необходимую информацию для правильной настройки каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="fc247-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="fc247-113">Существует два способа предоставить сведения о конфигурации во время логотипа:</span><span class="sxs-lookup"><span data-stu-id="fc247-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="fc247-114">Поставщик службы может получить сведения из профиля.</span><span class="sxs-lookup"><span data-stu-id="fc247-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="fc247-115">Поставщик услуг может затмить пользователя в запросе информации.</span><span class="sxs-lookup"><span data-stu-id="fc247-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="fc247-116">Так как второй вариант недоступен для автоматизированных клиентов, эти клиенты должны использовать первый вариант.</span><span class="sxs-lookup"><span data-stu-id="fc247-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="fc247-117">Клиенты должны тщательно настраивать свои профили, чтобы гарантировать, что этот параметр всегда работает.</span><span class="sxs-lookup"><span data-stu-id="fc247-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="fc247-118">Автоматические клиенты всегда устанавливают флаг MAPI_NO_MAIL в вызове функции [MAPILogonEx,](mapilogonex.md) чтобы начать сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="fc247-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

