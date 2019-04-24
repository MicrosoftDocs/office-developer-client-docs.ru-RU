---
title: Объекты поставщика транспорта MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357380"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="260e1-103">Объекты поставщика транспорта MAPI</span><span class="sxs-lookup"><span data-stu-id="260e1-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="260e1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="260e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="260e1-105">Помимо стандартных объектов provider и logon, реализованных всеми поставщиками услуг, для реализации объекта Status необходимы поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="260e1-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="260e1-106">Для других типов поставщиков услуг реализация объекта Status является необязательной.</span><span class="sxs-lookup"><span data-stu-id="260e1-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="260e1-107">Однако для поставщиков транспорта требуется MAPI.</span><span class="sxs-lookup"><span data-stu-id="260e1-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="260e1-108">Поставщики транспорта, поддерживающие загрузку заголовков сообщений с удаленного сервера, также реализуют папку и таблицу.</span><span class="sxs-lookup"><span data-stu-id="260e1-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="260e1-109">На следующем рисунке показаны все объекты, которые поставщики транспорта могут реализовать с помощью соответствующих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="260e1-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="260e1-110">На рисунке также показано, является ли MAPI или клиент пользователем объекта.</span><span class="sxs-lookup"><span data-stu-id="260e1-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="260e1-111">![Объекты, реализуемые поставщиками транспорта] (media/amapi_66.gif "Объекты, реализуемые поставщиками транспорта")</span><span class="sxs-lookup"><span data-stu-id="260e1-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="260e1-112">См. также</span><span class="sxs-lookup"><span data-stu-id="260e1-112">See also</span></span>

- [<span data-ttu-id="260e1-113">Объекты поставщика службы MAPI</span><span class="sxs-lookup"><span data-stu-id="260e1-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

