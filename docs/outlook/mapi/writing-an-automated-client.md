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
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812602"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="73c37-103">Написание автоматизированного клиента</span><span class="sxs-lookup"><span data-stu-id="73c37-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="73c37-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73c37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73c37-105">Автоматическая отправка клиентского приложения — это приложение, на котором выполняется в автоматическом режиме, пользовательский интерфейс не отображался.</span><span class="sxs-lookup"><span data-stu-id="73c37-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="73c37-106">По умолчанию множество методов интерфейса MAPI отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="73c37-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="73c37-107">Все эти методы имеют флаги, разрешающие клиента разрешить или отключить этот отображения.</span><span class="sxs-lookup"><span data-stu-id="73c37-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="73c37-108">Хотя MAPI ожидает поставщиков услуг принять следующие флаги, существуют некоторые поставщики, которые не всегда соответствовать этим требованиям.</span><span class="sxs-lookup"><span data-stu-id="73c37-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="73c37-109">Допустимым Причина не учитывая флаги — это расчет поставщика услуг на другой службы, которая не позволяет подавления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="73c37-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="73c37-110">При разработке автоматической клиента Обратите пристальное внимание для поставщиков услуг, которую вы используете и как они были настроены.</span><span class="sxs-lookup"><span data-stu-id="73c37-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="73c37-111">Не следует считать, что все звонки подавления пользовательского интерфейса будет выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="73c37-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="73c37-112">Автоматическая отправка клиенты должны иметь сведения, необходимые для правильной настройки каждого из службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="73c37-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="73c37-113">Существует два способа для предоставления сведений о конфигурации во время входа:</span><span class="sxs-lookup"><span data-stu-id="73c37-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="73c37-114">Поставщик услуг может получить сведения из профиля.</span><span class="sxs-lookup"><span data-stu-id="73c37-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="73c37-115">Поставщик услуг может запрашивать у пользователя сведения.</span><span class="sxs-lookup"><span data-stu-id="73c37-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="73c37-116">Так как второй параметр недоступен для автоматической клиентов, эти клиенты должны использовать первый вариант.</span><span class="sxs-lookup"><span data-stu-id="73c37-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="73c37-117">Клиенты необходимо настроить свой профиль, чтобы убедиться, что этот параметр всегда работает.</span><span class="sxs-lookup"><span data-stu-id="73c37-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="73c37-118">Автоматическая отправка клиентов всегда устанавливать флаг MAPI_NO_MAIL в вызове функции [MAPILogonEx](mapilogonex.md) для начала сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="73c37-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

