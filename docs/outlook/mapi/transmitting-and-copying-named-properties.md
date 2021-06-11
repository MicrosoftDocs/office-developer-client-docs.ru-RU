---
title: Передача и копирование именных свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437779"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="d808b-103">Передача и копирование именных свойств</span><span class="sxs-lookup"><span data-stu-id="d808b-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="d808b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d808b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d808b-105">При отправлении, перемещении или копировании имени имя остается неизменным, но идентификатор должен изменяться, чтобы соответствовать сопоставлению объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="d808b-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="d808b-106">Единственным исключением из этого правила является то, что источник и пункт назначения имеют ту же подпись сопоставления, что делает повторное повторное внесение ненужным.</span><span class="sxs-lookup"><span data-stu-id="d808b-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="d808b-107">Поставщик транспорта несет ответственность за перенаправление имен передаваемых имен свойств на соответствующие идентификаторы, которые работают в пункте назначения.</span><span class="sxs-lookup"><span data-stu-id="d808b-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="d808b-108">Поставщик транспорта отправки не может знать, какое правильное сопоставление находится в пункте назначения; он должен передавать имена и полагаться на поставщика транспорта, который получает, чтобы составить их в идентификаторы, которые работают.</span><span class="sxs-lookup"><span data-stu-id="d808b-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="d808b-109">Реализация TNEF MAPI обрабатывает повторное выполнение именных свойств для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="d808b-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="d808b-110">Поставщики транспорта могут обрабатывать повторное выполнение вручную или использовать реализацию TNEF.</span><span class="sxs-lookup"><span data-stu-id="d808b-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="d808b-111">Аналогичное повторное копирование именных свойств должно происходить при копировании этих свойств между хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="d808b-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="d808b-112">Однако, поскольку поставщики хранения сообщений могут получить имя для сопоставления идентификатора назначения, они могут сразу же переназначить свойства и не должны полагаться на хранилище сообщений назначения.</span><span class="sxs-lookup"><span data-stu-id="d808b-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d808b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d808b-113">See also</span></span>



[<span data-ttu-id="d808b-114">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d808b-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

