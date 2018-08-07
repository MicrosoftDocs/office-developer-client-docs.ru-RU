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
ms.openlocfilehash: 96bc2e58482ba259b14e820f3380978f80c542c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812467"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="162dd-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="162dd-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="162dd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="162dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="162dd-105">Стратегии тестирования отличаются в зависимости от того, разрабатывается клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="162dd-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="162dd-106">Так как для клиентского приложения требуется один или несколько поставщиков услуг для работы, клиенты должно тестироваться в среде с различных наборов поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="162dd-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="162dd-107">Тем не менее, поставщиков услуг, следует выполнить проверку по отдельности перед интеграции с другими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="162dd-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="162dd-108">MAPI предоставляет средства, предназначенные для проверки возможностей поставщика услуг определенного типа.</span><span class="sxs-lookup"><span data-stu-id="162dd-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="162dd-109">Пример приложения [mfcmapi (en)](http://go.microsoft.com/fwlink/?LinkId=124154) показывается, как для тестирования функции поставщика адресных книг и поставщик хранилища работает с сообщением.</span><span class="sxs-lookup"><span data-stu-id="162dd-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="162dd-110">См. также</span><span class="sxs-lookup"><span data-stu-id="162dd-110">See also</span></span>



[<span data-ttu-id="162dd-111">����� �������� � ���������������� MAPI</span><span class="sxs-lookup"><span data-stu-id="162dd-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="162dd-112">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="162dd-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

