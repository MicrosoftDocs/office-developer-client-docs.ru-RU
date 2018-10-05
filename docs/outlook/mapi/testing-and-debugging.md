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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383662"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="39078-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="39078-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="39078-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39078-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39078-105">Стратегии тестирования отличаются в зависимости от того, разрабатывается клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="39078-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="39078-106">Так как для клиентского приложения требуется один или несколько поставщиков услуг для работы, клиенты должно тестироваться в среде с различных наборов поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="39078-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="39078-107">Тем не менее, поставщиков услуг, следует выполнить проверку по отдельности перед интеграции с другими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="39078-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="39078-108">MAPI предоставляет средства, предназначенные для проверки возможностей поставщика услуг определенного типа.</span><span class="sxs-lookup"><span data-stu-id="39078-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="39078-109">Пример приложения [mfcmapi (en)](https://go.microsoft.com/fwlink/?LinkId=124154) показывается, как для тестирования функции поставщика адресных книг и поставщик хранилища работает с сообщением.</span><span class="sxs-lookup"><span data-stu-id="39078-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39078-110">См. также</span><span class="sxs-lookup"><span data-stu-id="39078-110">See also</span></span>



[<span data-ttu-id="39078-111">����� �������� � ���������������� MAPI</span><span class="sxs-lookup"><span data-stu-id="39078-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="39078-112">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="39078-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

