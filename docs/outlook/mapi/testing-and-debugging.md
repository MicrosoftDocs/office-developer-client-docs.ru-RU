---
title: Тестирование и отладка
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8e1f15ae354894aede4e8418e6428d0524ccb70d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316487"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="144dd-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="144dd-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="144dd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="144dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="144dd-105">Стратегии тестирования различаются в зависимости от того, разрабатывается ли клиент или поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="144dd-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="144dd-106">Так как для клиентского приложения требуется, чтобы один или несколько поставщиков служб работали, клиенты должны тестироваться в среде с разными наборами поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="144dd-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="144dd-107">Однако поставщики услуг необходимо протестировать в изоляции, прежде чем они будут интегрированы с другими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="144dd-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="144dd-108">MAPI предоставляет средства, предназначенные для тестирования функций поставщика услуг определенного типа.</span><span class="sxs-lookup"><span data-stu-id="144dd-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="144dd-109">В примере приложения [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) показано, как проверить возможности поставщика адресных книг и работать с поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="144dd-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="144dd-110">См. также</span><span class="sxs-lookup"><span data-stu-id="144dd-110">See also</span></span>



[<span data-ttu-id="144dd-111">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="144dd-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="144dd-112">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="144dd-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

