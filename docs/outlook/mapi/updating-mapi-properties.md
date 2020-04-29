---
title: Обновление свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407524"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="53d43-103">Обновление свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="53d43-103">Updating MAPI properties</span></span>

<span data-ttu-id="53d43-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53d43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53d43-105">Клиенты и поставщики услуг могут обновлять значение свойства с помощью вызова:</span><span class="sxs-lookup"><span data-stu-id="53d43-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="53d43-106">Метод объекта [IMAPIProp:: SetProps](imapiprop-setprops.md) для обновления значения одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="53d43-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="53d43-107">Функция [хрсетонепроп](hrsetoneprop.md) для обновления только одного свойства за раз.</span><span class="sxs-lookup"><span data-stu-id="53d43-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="53d43-108">Используйте **хрсетонепроп** только в том случае, если целевой объект является локальным; Эта функция может привести к ухудшению производительности при использовании с удаленными объектами.</span><span class="sxs-lookup"><span data-stu-id="53d43-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="53d43-109">В следующей процедуре показано, как использовать **SetProps** для обновления класса Message или свойства PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения.</span><span class="sxs-lookup"><span data-stu-id="53d43-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="53d43-110">Обновление класса сообщения сообщения</span><span class="sxs-lookup"><span data-stu-id="53d43-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="53d43-111">Выделить структуру [спропвалуе](spropvalue.md) для класса сообщений и присвоить ей соответствующие элементы.</span><span class="sxs-lookup"><span data-stu-id="53d43-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="53d43-112">Вызовите метод сообщения **IMAPIProp:: SetProps** , чтобы задать новый класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="53d43-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="53d43-113">См. также</span><span class="sxs-lookup"><span data-stu-id="53d43-113">See also</span></span>

- [<span data-ttu-id="53d43-114">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="53d43-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

