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
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812539"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="e46a0-103">Обновление свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="e46a0-103">Updating MAPI properties</span></span>

<span data-ttu-id="e46a0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e46a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e46a0-105">Клиенты и поставщиков услуг можно обновить значение свойства, вызывая:</span><span class="sxs-lookup"><span data-stu-id="e46a0-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="e46a0-106">Метод [IMAPIProp::SetProps](imapiprop-setprops.md) объекта обновление значения одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="e46a0-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="e46a0-107">Функция [HrSetOneProp](hrsetoneprop.md) для обновления только одно свойство за раз.</span><span class="sxs-lookup"><span data-stu-id="e46a0-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="e46a0-108">Используйте **HrSetOneProp** только в том случае, если целевой объект является локальным; Эта функция может привести к снижению производительности при использовании с удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="e46a0-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="e46a0-109">В следующей процедуре показано, как использовать **SetProps** для обновления класса сообщений или свойство PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), сообщения.</span><span class="sxs-lookup"><span data-stu-id="e46a0-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="e46a0-110">Чтобы обновить класс сообщения сообщения</span><span class="sxs-lookup"><span data-stu-id="e46a0-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="e46a0-111">Выделите структуру [SPropValue](spropvalue.md) для класса сообщения и задать его члены соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="e46a0-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="e46a0-112">Вызовите метод **IMAPIProp::SetProps** сообщения, чтобы задать новый класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="e46a0-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="e46a0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e46a0-113">See also</span></span>

- [<span data-ttu-id="e46a0-114">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="e46a0-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

