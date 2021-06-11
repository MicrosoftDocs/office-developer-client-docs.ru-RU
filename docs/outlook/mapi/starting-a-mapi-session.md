---
title: Запуск сеанса MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336346"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="9e8aa-103">Запуск сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="9e8aa-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="9e8aa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e8aa-105">Несмотря на то, что во время запуска сеанса выполняется значительный объем работы, необходимые задачи минимальны.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="9e8aa-106">Большая часть этой работы делается в обработке MAPI вызовов [MAPIInitialize](mapiinitialize.md) и [MAPILogonEx.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="9e8aa-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="9e8aa-107">Обе эти функции принимают флаги в качестве параметров ввода для управления аспектами сеанса, такими как обработка уведомлений и пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="9e8aa-108">Важно понимать последствия установки каждого из этих флагов при вызове **MAPIInitialize** для инициализации библиотек MAPI и **MAPILogonEx** для входа в подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="9e8aa-109">**Запуск сеанса MAPI**</span><span class="sxs-lookup"><span data-stu-id="9e8aa-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="9e8aa-110">Вызов **MAPIInitialize,** чтобы инициализировать стандартный набор библиотек MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="9e8aa-111">Если вам нужно использовать библиотеки OLE, позвоните в OLE-функцию [OleInitialize.](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e8aa-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="9e8aa-112">Если вам нужно использовать библиотеку утилиты MAPI, позвоните [в ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="9e8aa-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="9e8aa-113">Вызов **MAPILogonEx с** допустимым профилем для входа в подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="9e8aa-114">**MAPILogonEx** проверяет конфигурацию каждого из поставщиков услуг в службах сообщений, включенных в профиль, и, при необходимости, запросит у пользователя дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="9e8aa-115">После **завершения MAPILogonEx** настроенные поставщики услуг готовы к обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="9e8aa-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9e8aa-116">In this section</span></span>

[<span data-ttu-id="9e8aa-117">Инициализация MAPI</span><span class="sxs-lookup"><span data-stu-id="9e8aa-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="9e8aa-118">Описывает инициализацию MAPI для сеанса.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="9e8aa-119">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="9e8aa-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="9e8aa-120">Описывает вызовы, которые необходимо сделать для инициализации OLE для использования с MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="9e8aa-121">Инициализация утилит MAPI</span><span class="sxs-lookup"><span data-stu-id="9e8aa-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="9e8aa-122">Описывает инициализацию утилит MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="9e8aa-123">Вход в MAPI</span><span class="sxs-lookup"><span data-stu-id="9e8aa-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="9e8aa-124">Описывает, как клиентские приложения войдите в подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

