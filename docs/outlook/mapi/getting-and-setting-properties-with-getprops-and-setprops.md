---
title: Получение и установка свойств с помощью методов GetProps и SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299400"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="88f10-103">Получение и установка свойств с помощью методов GetProps и SetProps</span><span class="sxs-lookup"><span data-stu-id="88f10-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="88f10-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88f10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88f10-105">Когда это возможно, попробуйте получить или изменить свойство с помощью методов [IMAPIProp::](imapiprop-getprops.md) IMAPIProp и [:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="88f10-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="88f10-106">Если свойство, с которым вы работаете, слишком велико, эти методы должны быть достаточными.</span><span class="sxs-lookup"><span data-stu-id="88f10-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="88f10-107">Другой альтернативой является считывание из потока и запись в него с помощью интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="88f10-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="88f10-108">Потоки могут успешно обрабатывать очень большие свойства, но они больше очищаются по ресурсам, так как они нуждаются в библиотеках COM.</span><span class="sxs-lookup"><span data-stu-id="88f10-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="88f10-109">Используйте интерфейс **IStream** только после вызова **IMAPIProp:: PROPS** или **IMAPIProp:: SetProps** не работает.</span><span class="sxs-lookup"><span data-stu-id="88f10-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

