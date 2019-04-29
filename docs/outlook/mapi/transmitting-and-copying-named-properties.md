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
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437779"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="46506-103">Передача и копирование именованных свойств</span><span class="sxs-lookup"><span data-stu-id="46506-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="46506-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46506-105">Всякий раз, когда именованное свойство отправляется, перемещается или копируется, оно остается неизменным, но идентификатор должен измениться, чтобы придерживаться сопоставления целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="46506-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="46506-106">Единственное исключение из этого правила состоит в том, что исходный и целевой подписи сопоставления имеют одинаковую сигнатуру сопоставления, что делает повторное сопоставление ненужным.</span><span class="sxs-lookup"><span data-stu-id="46506-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="46506-107">Поставщик транспорта отвечает за сопоставление имен переданных именованных свойств с соответствующими идентификаторами, которые работают в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="46506-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="46506-108">Отправляющий поставщик транспорта не может определить правильное сопоставление в месте назначения; Он должен передать имена и полагаться на принимающий поставщик транспорта, чтобы сопоставить их с идентификаторами, которые работают.</span><span class="sxs-lookup"><span data-stu-id="46506-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="46506-109">Реализация формата TNEF в MAPI обрабатывает изменение сопоставления именованных свойств для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="46506-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="46506-110">Поставщики транспорта могут либо обработать повторное сопоставление вручную, либо использовать реализацию TNEF.</span><span class="sxs-lookup"><span data-stu-id="46506-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="46506-111">Аналогичное пересопоставление именованных свойств должно происходить при копировании этих свойств между хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="46506-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="46506-112">Тем не менее, так как поставщики хранилищ сообщений могут извлекать имя по идентификатору назначения, они могут повторно сопоставить свойства и не должны полагаться на конечное хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="46506-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46506-113">См. также</span><span class="sxs-lookup"><span data-stu-id="46506-113">See also</span></span>



[<span data-ttu-id="46506-114">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="46506-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

