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
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812377"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="65a5b-103">Запуск сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="65a5b-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="65a5b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65a5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65a5b-105">Хотя значительное выполненных во время сеанса запуска работ, необходимых задач минимальны.</span><span class="sxs-lookup"><span data-stu-id="65a5b-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="65a5b-106">Большая часть этой работы выполняется в MAPI обработки вызовов [MAPIInitialize](mapiinitialize.md) и [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="65a5b-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="65a5b-107">Обе эти функции принимать флаги в качестве входных параметров для управления аспектов сеанса, таких как обработки уведомлений и пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="65a5b-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="65a5b-108">Важно понять последствия настройки каждой из этих флагов при вызове **MAPIInitialize** для инициализации библиотеки MAPI и **MAPILogonEx** войдите в систему в подсистеме MAPI.</span><span class="sxs-lookup"><span data-stu-id="65a5b-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="65a5b-109">**Начало сеанса MAPI**</span><span class="sxs-lookup"><span data-stu-id="65a5b-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="65a5b-110">Вызов **MAPIInitialize** для инициализации стандартный набор библиотек MAPI.</span><span class="sxs-lookup"><span data-stu-id="65a5b-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="65a5b-111">Если необходимо использовать библиотек OLE, вызовите функцию OLE [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="65a5b-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="65a5b-112">Если требуется использовать библиотеку служебной программы MAPI, вызовите [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="65a5b-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="65a5b-113">Вызов **MAPILogonEx** с допустимого профиля войдите в систему в подсистеме MAPI.</span><span class="sxs-lookup"><span data-stu-id="65a5b-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="65a5b-114">**MAPILogonEx** проверяет конфигурацию каждый из поставщиков услуг в службах сообщения, включенные в профиль, запросом для получения дополнительных сведений, если необходимо и возможные.</span><span class="sxs-lookup"><span data-stu-id="65a5b-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="65a5b-115">По завершении **MAPILogonEx** поставщиков услуг настроенного готовы для службы.</span><span class="sxs-lookup"><span data-stu-id="65a5b-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="65a5b-116">В этой статье</span><span class="sxs-lookup"><span data-stu-id="65a5b-116">In this section</span></span>

[<span data-ttu-id="65a5b-117">Инициализация MAPI</span><span class="sxs-lookup"><span data-stu-id="65a5b-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="65a5b-118">Описание способов инициализации MAPI для сеанса.</span><span class="sxs-lookup"><span data-stu-id="65a5b-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="65a5b-119">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="65a5b-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="65a5b-120">Описание вызовов для выполнения инициализировать OLE для использования с MAPI.</span><span class="sxs-lookup"><span data-stu-id="65a5b-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="65a5b-121">Инициализация служебных программ MAPI</span><span class="sxs-lookup"><span data-stu-id="65a5b-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="65a5b-122">Описание способов инициализации MAPI служебных программ.</span><span class="sxs-lookup"><span data-stu-id="65a5b-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="65a5b-123">Вход в MAPI</span><span class="sxs-lookup"><span data-stu-id="65a5b-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="65a5b-124">Описывает, как клиентские приложения выполните вход в систему sub MAPI.</span><span class="sxs-lookup"><span data-stu-id="65a5b-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

