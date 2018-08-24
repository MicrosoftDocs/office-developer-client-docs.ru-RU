---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 36b8381e2bf98f5ddcb88a54b56f2b5c91b3b668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572601"
---
# <a name="notifkey"></a><span data-ttu-id="112c2-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="112c2-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="112c2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="112c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="112c2-105">Однозначно определяет подключение между приемника уведомления, источник уведомлений и MAPI.</span><span class="sxs-lookup"><span data-stu-id="112c2-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="112c2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="112c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="112c2-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="112c2-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="112c2-108">Members</span><span class="sxs-lookup"><span data-stu-id="112c2-108">Members</span></span>

 <span data-ttu-id="112c2-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="112c2-109">**cb**</span></span>
  
> <span data-ttu-id="112c2-110">Число байт в член **ab** .</span><span class="sxs-lookup"><span data-stu-id="112c2-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="112c2-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="112c2-111">**ab**</span></span>
  
> <span data-ttu-id="112c2-112">Массив байтов, описывающее ключ уведомлений.</span><span class="sxs-lookup"><span data-stu-id="112c2-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="112c2-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="112c2-113">Remarks</span></span>

<span data-ttu-id="112c2-114">[Подписки на](imapisupport-subscribe.md) и [Уведомлять](imapisupport-notify.md) методы [IMAPISupport](imapisupportiunknown.md) использовать структуру **NOTIFKEY** для создания уведомлений на приемник соответствующих уведомлений об источнике соответствующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="112c2-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="112c2-115">Поставщики услуг создания ключей уведомлений при их вызывается метод **уведомлений** и их нужно Позвонить **подписки на** для обработки регистрации уведомлений и последующие отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="112c2-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="112c2-116">Клавиша уведомление может быть идентификатор записи источника уведомлений или может быть любой идентификационные элемент таких как константа.</span><span class="sxs-lookup"><span data-stu-id="112c2-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="112c2-117">Например поставщик хранения сообщений использовать путь к папке ключом уведомлений.</span><span class="sxs-lookup"><span data-stu-id="112c2-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="112c2-118">Клавиша уведомлений должны работать на несколько процессов.</span><span class="sxs-lookup"><span data-stu-id="112c2-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="112c2-119">Требования к области уведомлений ключа похожи для долгосрочного идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="112c2-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="112c2-120">Тем не менее в отличие от идентификатор записи уведомлений ключ должен быть сравнимые двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="112c2-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="112c2-121">Как правило ключ уведомлений включает в себя значение **GUID** , определенные поставщиком услуг, следуют другие сведения о поставщике уникальный объект.</span><span class="sxs-lookup"><span data-stu-id="112c2-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="112c2-122">Обсуждение использования структуры **NOTIFKEY** для управления соединения между приемники уведомлений и объекты, которые создают уведомления, в разделе [Поддержка уведомления о событии](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="112c2-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="112c2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="112c2-123">See also</span></span>



[<span data-ttu-id="112c2-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="112c2-124">MAPI Structures</span></span>](mapi-structures.md)

