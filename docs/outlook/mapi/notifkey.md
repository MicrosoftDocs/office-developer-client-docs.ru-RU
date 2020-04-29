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
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429630"
---
# <a name="notifkey"></a><span data-ttu-id="a0d5e-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="a0d5e-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="a0d5e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0d5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0d5e-105">Уникально идентифицирует соединение между приемником уведомлений, источником уведомлений и MAPI.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0d5e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a0d5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0d5e-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="a0d5e-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="a0d5e-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a0d5e-108">Members</span></span>

 <span data-ttu-id="a0d5e-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="a0d5e-109">**cb**</span></span>
  
> <span data-ttu-id="a0d5e-110">Количество байтов в элементе **AB** .</span><span class="sxs-lookup"><span data-stu-id="a0d5e-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="a0d5e-111">**поисков**</span><span class="sxs-lookup"><span data-stu-id="a0d5e-111">**ab**</span></span>
  
> <span data-ttu-id="a0d5e-112">Массив байтов, описывающих ключ уведомления.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0d5e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0d5e-113">Remarks</span></span>

<span data-ttu-id="a0d5e-114">Методы [Subscribe](imapisupport-subscribe.md) и [Notify](imapisupport-notify.md) [имаписуппорт](imapisupportiunknown.md) используют структуру **нотифкэй** для создания уведомлений о соответствующем источнике уведомлений в соответствующем приемнике уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="a0d5e-115">Поставщики услуг создают ключи уведомлений при вызове метода **advise** и хотят вызывать **подписку** , чтобы обрабатывать регистрацию уведомлений и дальнейшую отправку уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="a0d5e-116">Ключ уведомления может быть идентификатором источника уведомления или любым другим идентифицирующим элементом, таким как константа.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="a0d5e-117">Например, поставщик хранилища сообщений может использовать путь к папке в качестве ключа уведомления.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="a0d5e-118">Ключ уведомления должен работать в нескольких процессах.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="a0d5e-119">Требования к области для ключа уведомления похожи на идентификаторы долгосрочных записей.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="a0d5e-120">Тем не менее, в отличие от идентификатора записи, ключ уведомления должен быть двоично сравнимым.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="a0d5e-121">Как правило, ключ уведомления содержит значение **GUID** , определенное поставщиком услуг, за которым следуют другие сведения, относящиеся к конкретному поставщику, которые являются уникальными для объекта.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="a0d5e-122">Сведения о том, как использовать структуру **нотифкэй** для управления подключениями между приемниками уведомлений и объектами, которые создают уведомления, приведены в статье [Поддержка уведомлений о событиях](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="a0d5e-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0d5e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a0d5e-123">See also</span></span>



[<span data-ttu-id="a0d5e-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a0d5e-124">MAPI Structures</span></span>](mapi-structures.md)

