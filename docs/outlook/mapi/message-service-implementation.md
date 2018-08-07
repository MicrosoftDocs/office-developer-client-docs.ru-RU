---
title: Реализация службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810012"
---
# <a name="message-service-implementation"></a><span data-ttu-id="465a0-103">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="465a0-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="465a0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="465a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="465a0-105">Служба сообщений — один или несколько поставщиков услуг, связанных с ними, сгруппированная для упрощения процесса установки и настройки.</span><span class="sxs-lookup"><span data-stu-id="465a0-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="465a0-106">Все поставщики услуг должно быть включено в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="465a0-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="465a0-107">Для реализации службы сообщений с помощью одного или нескольких поставщиков, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="465a0-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="465a0-108">Разработка служба сообщений, определение числа и типа поставщиков услуг, которые требуется включить.</span><span class="sxs-lookup"><span data-stu-id="465a0-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="465a0-109">Дополнительные сведения о создании службы сообщений [Службы сообщений](designing-a-message-service.md)см.</span><span class="sxs-lookup"><span data-stu-id="465a0-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="465a0-110">Создайте программу установки для поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="465a0-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="465a0-111">Дополнительные сведения о записи программы установки службы сообщений можно [Поддержки установки службы сообщений](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="465a0-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="465a0-112">Создайте функцию точки входа для выполнения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="465a0-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="465a0-113">Дополнительные сведения о создании записи службы сообщений точки функция см [MSGSERVICEENTRY](msgserviceentry.md)и [Поддержки конфигурации службы сообщений](supporting-message-service-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="465a0-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="465a0-114">Создайте файл общедоступных заголовка, который содержит свойство теги и описания допустимых значений для все настраиваемые свойства, которые поддерживает службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="465a0-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="465a0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="465a0-115">See also</span></span>



[<span data-ttu-id="465a0-116">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="465a0-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

