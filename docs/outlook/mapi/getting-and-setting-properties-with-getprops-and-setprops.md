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
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395009"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="1f297-103">Получение и задание свойств с помощью GetProps и SetProps</span><span class="sxs-lookup"><span data-stu-id="1f297-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="1f297-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f297-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f297-105">Когда это возможно, попробуйте для извлечения или изменения свойства с помощью методов [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="1f297-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="1f297-106">Если свойство, с которым вы работаете с очень большой, должно быть достаточно эти методы.</span><span class="sxs-lookup"><span data-stu-id="1f297-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="1f297-107">Альтернативой является чтение или запись к потоку с помощью интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1f297-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="1f297-108">Потоки, может обрабатывать очень большой свойства успешно, но они являются более высокой версии затрат на ресурсы, так как они требуют библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="1f297-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="1f297-109">С помощью интерфейса **IStream** только после сбоя при вызове **IMAPIProp::GetProps** или **IMAPIProp::SetProps** .</span><span class="sxs-lookup"><span data-stu-id="1f297-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

