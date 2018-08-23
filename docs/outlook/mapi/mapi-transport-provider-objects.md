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
ms.openlocfilehash: de0334ee9a90da38e472571314136195c84a7866
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592705"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="d570d-103">Объекты поставщика транспорта MAPI</span><span class="sxs-lookup"><span data-stu-id="d570d-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="d570d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d570d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d570d-105">В дополнение к стандартный поставщик и объектов входа в систему, реализованных всех поставщиков услуг поставщиками транспорта необходимы для реализации объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="d570d-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="d570d-106">Для других типов поставщика службы реализация объекта состояние является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d570d-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="d570d-107">Тем не менее MAPI он необходим для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="d570d-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="d570d-108">Поставщики транспорта, которые поддерживают загрузку заголовков сообщений с удаленного сервера также реализовать папки и таблицы.</span><span class="sxs-lookup"><span data-stu-id="d570d-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="d570d-109">На следующем рисунке показана объектам, которые можно реализовать транспорта поставщиков с их соответствующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d570d-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="d570d-110">Иллюстрация также указывает, является ли MAPI или клиента объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="d570d-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="d570d-111">![Объекты, реализуемые поставщиками транспорта] (media/amapi_66.gif "Объекты, реализуемые поставщиками транспорта")</span><span class="sxs-lookup"><span data-stu-id="d570d-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d570d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d570d-112">See also</span></span>

- [<span data-ttu-id="d570d-113">Объекты поставщика службы MAPI</span><span class="sxs-lookup"><span data-stu-id="d570d-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

