---
title: Передача и копирование именованных свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587518"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="15084-103">Передача и копирование именованных свойств</span><span class="sxs-lookup"><span data-stu-id="15084-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="15084-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15084-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15084-105">Каждый раз, когда отправляется именованного свойства, переместить или скопировать, имя не изменяется, но идентификатор необходимо изменить в соответствии сопоставления в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="15084-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="15084-106">Единственным исключением из этого правила является при исходном и целевом иметь ту же подпись сопоставления внесения сопоставление ненужных.</span><span class="sxs-lookup"><span data-stu-id="15084-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="15084-107">Это ответственность за поставщика транспорта сопоставление имен передаваемых именованных свойств, соответствующие идентификаторы, которые работают в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="15084-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="15084-108">Отправка поставщика транспорта не удается возможности, правильное сопоставление на целевом сервере; он должен передавать имена и основаны на получение поставщика транспорта, чтобы сопоставить их с идентификаторами, которые работают.</span><span class="sxs-lookup"><span data-stu-id="15084-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="15084-109">Реализация интерфейса MAPI TNEF обрабатывает сопоставление именованного свойства для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="15084-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="15084-110">Поставщики транспорта можно обрабатывать сопоставление вручную или с помощью реализации TNEF.</span><span class="sxs-lookup"><span data-stu-id="15084-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="15084-111">Аналогично сопоставления именованных свойств должно выполняться при копировании эти свойства между хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="15084-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="15084-112">Тем не менее так как поставщиков хранилища сообщений можно получить имя, идентификатор сопоставления назначения, они немедленно осуществить повторное сопоставление свойства и не зависящие от хранилища сообщений назначения.</span><span class="sxs-lookup"><span data-stu-id="15084-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15084-113">См. также</span><span class="sxs-lookup"><span data-stu-id="15084-113">See also</span></span>



[<span data-ttu-id="15084-114">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15084-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

