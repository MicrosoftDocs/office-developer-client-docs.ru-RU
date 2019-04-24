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
# <a name="starting-a-mapi-session"></a><span data-ttu-id="abcad-103">Запуск сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="abcad-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="abcad-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abcad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abcad-105">Хотя при запуске сеанса существует значительный объем работы, обязательные задачи минимальны.</span><span class="sxs-lookup"><span data-stu-id="abcad-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="abcad-106">Значительная часть этой работы выполняется при обработке MAPI вызовов [мапиинитиализе](mapiinitialize.md) и [мапилогонекс](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="abcad-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="abcad-107">Обе эти функции принимают флаги в качестве входных параметров для управления аспектами сеанса, такими как обработка уведомлений и пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="abcad-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="abcad-108">Важно понимать последствия установки каждого из этих флагов при вызове **мапиинитиализе** для инициализации библиотек MAPI и **мапилогонекс** для входа в подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="abcad-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="abcad-109">**Запуск сеанса MAPI**</span><span class="sxs-lookup"><span data-stu-id="abcad-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="abcad-110">Call **мапиинитиализе** для инициализации стандартного набора библиотек MAPI.</span><span class="sxs-lookup"><span data-stu-id="abcad-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="abcad-111">Если вам нужно использовать библиотеки OLE, вызовите функцию OLE [олеинитиализе](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="abcad-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="abcad-112">Если требуется использовать библиотеку служебной программы MAPI, вызовите [сЦинитмапиутил](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="abcad-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="abcad-113">ВыЗовите **мапилогонекс** с допустимым профилем, чтобы войти в подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="abcad-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="abcad-114">**Мапилогонекс** проверяет конфигурацию каждого поставщика услуг в службах сообщений, включенных в профиль, и запрашивает у пользователя дополнительные сведения, если это необходимо и возможно.</span><span class="sxs-lookup"><span data-stu-id="abcad-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="abcad-115">После завершения **мапилогонекс** настроенные поставщики услуг готовы к обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="abcad-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="abcad-116">Содержание</span><span class="sxs-lookup"><span data-stu-id="abcad-116">In this section</span></span>

[<span data-ttu-id="abcad-117">Инициализация MAPI</span><span class="sxs-lookup"><span data-stu-id="abcad-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="abcad-118">В этой статье описывается, как инициализировать MAPI для сеанса.</span><span class="sxs-lookup"><span data-stu-id="abcad-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="abcad-119">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="abcad-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="abcad-120">В этой статье описываются вызовы, которые необходимо выполнить, чтобы инициализировать OLE для использования с MAPI.</span><span class="sxs-lookup"><span data-stu-id="abcad-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="abcad-121">Инициализация служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="abcad-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="abcad-122">В этой статье описывается инициализация служебных программ MAPI.</span><span class="sxs-lookup"><span data-stu-id="abcad-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="abcad-123">Вход в MAPI</span><span class="sxs-lookup"><span data-stu-id="abcad-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="abcad-124">Описывает, как клиентские приложения выполняют вход в подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="abcad-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

