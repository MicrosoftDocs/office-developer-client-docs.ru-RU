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
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356919"
---
# <a name="message-service-implementation"></a><span data-ttu-id="31055-103">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="31055-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="31055-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31055-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31055-105">Служба сообщений является одним или несколькими связанными поставщиками услуг, сгруппированными вместе для упрощения установки и настройки.</span><span class="sxs-lookup"><span data-stu-id="31055-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="31055-106">Все поставщики услуг должны быть включены в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="31055-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="31055-107">Чтобы реализовать службу сообщений с одним или несколькими поставщиками, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="31055-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="31055-108">РазРаботайте службу сообщений, определяя число и тип включаемых поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="31055-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="31055-109">Дополнительные сведения о разработке службы сообщений можно найти в статье [Разработка службы сообщений](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="31055-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="31055-110">Создайте программу установки для установки поставщиков услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="31055-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="31055-111">Более подробную информацию о создании программы установки службы сообщений можно узнать в разделе [Поддержка установки службы сообщений](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="31055-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="31055-112">Создайте функцию точки входа для выполнения настройки.</span><span class="sxs-lookup"><span data-stu-id="31055-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="31055-113">Дополнительные сведения о написании функции точки входа службы сообщений: [Поддержка настройки службы сообщений](supporting-message-service-configuration.md) и [мсгсервицеентри](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="31055-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="31055-114">Создайте файл общедоступного заголовка, который содержит теги свойств и описания допустимых значений для всех настраиваемых свойств, поддерживаемых службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="31055-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="31055-115">См. также</span><span class="sxs-lookup"><span data-stu-id="31055-115">See also</span></span>



[<span data-ttu-id="31055-116">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="31055-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

