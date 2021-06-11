---
title: Пример надстройки состояния в автономном режиме
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a6bdf408-114a-2203-189f-101251a65a8c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf8e647af4aba53dfc24880e6ff491985b50a613
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431185"
---
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="69043-103">Пример надстройки состояния в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="69043-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="69043-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69043-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69043-105">API состояния автономного доступа поддерживает вызовы, указывающие на изменения в состоянии подключения пользователя в Outlook, например, от подключения к сети в Outlook до отключения.</span><span class="sxs-lookup"><span data-stu-id="69043-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="69043-106">Пример надстройки состояния в автономном режиме — это надстройка COM, написанная в C++ и демонстрирующая получение уведомлений об изменениях состояния подключения и изменение текущего состояния с помощью API состояния автономного доступа.</span><span class="sxs-lookup"><span data-stu-id="69043-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="69043-107">Дополнительные сведения об API автономного режима см. в статье [Об API автономного режима](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="69043-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="69043-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="69043-108">In this section</span></span>

- [<span data-ttu-id="69043-109">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="69043-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="69043-110">Объясняет, как скачать и установить надстройку Sample Offline State.</span><span class="sxs-lookup"><span data-stu-id="69043-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="69043-111">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="69043-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="69043-112">Описывает, как реализовать функции подключения, инициализации и настройки для использования надстройки автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="69043-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="69043-113">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="69043-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="69043-114">Описывает, как использовать функцию **[HrOpenOfflineObj](hropenofflineobj.md)** для получения автономного объекта для мониторинга и изменения состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="69043-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="69043-115">Отключение надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="69043-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="69043-116">Описывает, как правильно завершить и очистить надстройку автономного состояния при отключении надстройки.</span><span class="sxs-lookup"><span data-stu-id="69043-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69043-117">См. также</span><span class="sxs-lookup"><span data-stu-id="69043-117">See also</span></span>



[<span data-ttu-id="69043-118">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="69043-118">About the Offline State API</span></span>](about-the-offline-state-api.md)

