---
title: Пример надстройки автономного состояния
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
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="ca2f5-103">Пример надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="ca2f5-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="ca2f5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca2f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca2f5-105">API автономного состояния поддерживает вызовы, указывающие на изменения состояния подключения пользователя в Outlook, например от подключения к Сети в Outlook до отключения.</span><span class="sxs-lookup"><span data-stu-id="ca2f5-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="ca2f5-106">Пример надстройки автономного состояния — это надстройка COM, написанная на C++, которая демонстрирует получение уведомлений об изменениях состояния подключения и изменение текущего состояния с помощью API автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="ca2f5-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="ca2f5-107">Дополнительные сведения об API автономного режима см. в статье [Об API автономного режима](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="ca2f5-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ca2f5-108">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="ca2f5-108">In this section</span></span>

- [<span data-ttu-id="ca2f5-109">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="ca2f5-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="ca2f5-110">Объясняется, как скачать и установить пример надстройки автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="ca2f5-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="ca2f5-111">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="ca2f5-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="ca2f5-112">Описывается реализация функций подключения, инициализации и настройки для использования надстройки автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="ca2f5-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="ca2f5-113">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="ca2f5-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="ca2f5-114">Описывается, как использовать функцию **[HrOpenOfflineObj](hropenofflineobj.md)** для получения автономного объекта для отслеживания и изменения состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="ca2f5-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="ca2f5-115">Отключение надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="ca2f5-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="ca2f5-116">Описывает, как надлежащим образом завершить и очистить надстройку автономного состояния, когда надстройка отключена.</span><span class="sxs-lookup"><span data-stu-id="ca2f5-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca2f5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ca2f5-117">See also</span></span>



[<span data-ttu-id="ca2f5-118">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="ca2f5-118">About the Offline State API</span></span>](about-the-offline-state-api.md)

