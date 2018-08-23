---
title: Получение и задание свойств с помощью GetProps и SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6b54be711d8c33648d211e480c6a00ee92755108
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575569"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="4527a-103">Получение и задание свойств с помощью GetProps и SetProps</span><span class="sxs-lookup"><span data-stu-id="4527a-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="4527a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4527a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4527a-105">Когда это возможно, попробуйте для извлечения или изменения свойства с помощью методов [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="4527a-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="4527a-106">Если свойство, с которым вы работаете с очень большой, должно быть достаточно эти методы.</span><span class="sxs-lookup"><span data-stu-id="4527a-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="4527a-107">Альтернативой является чтение или запись к потоку с помощью интерфейса [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4527a-107">The other alternative is to read from or write to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="4527a-108">Потоки, может обрабатывать очень большой свойства успешно, но они являются более высокой версии затрат на ресурсы, так как они требуют библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="4527a-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="4527a-109">С помощью интерфейса **IStream** только после сбоя при вызове **IMAPIProp::GetProps** или **IMAPIProp::SetProps** .</span><span class="sxs-lookup"><span data-stu-id="4527a-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

