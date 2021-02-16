---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432207"
---
# <a name="mapiuid"></a><span data-ttu-id="a5cce-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a5cce-103">MAPIUID</span></span>

  
  
<span data-ttu-id="a5cce-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5cce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5cce-105">Независимая от по порядку версия [структуры GUID,](guid.md) используемая для уникальной идентификации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a5cce-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5cce-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a5cce-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5cce-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5cce-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a5cce-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="a5cce-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a5cce-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="a5cce-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="a5cce-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a5cce-110">Members</span></span>

 <span data-ttu-id="a5cce-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="a5cce-111">**ab**</span></span>
  
> <span data-ttu-id="a5cce-112">Массив, содержащий 16-byte identifier.</span><span class="sxs-lookup"><span data-stu-id="a5cce-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5cce-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5cce-113">Remarks</span></span>

<span data-ttu-id="a5cce-114">Структура **MAPIUID** — это **структура GUID,** помещаемая в ® процессора Intel.</span><span class="sxs-lookup"><span data-stu-id="a5cce-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="a5cce-115">MAPI создает структуры **MAPIUID** таким образом, что для двух разных элементов очень редко требуется один и тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a5cce-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="a5cce-116">**Структуры MAPIUID** могут храниться в двоичных свойствах или в качестве файлов без упорядочения в зависимости от порядка вбайтов компьютера, на который хранится информация, или доступа к ним.</span><span class="sxs-lookup"><span data-stu-id="a5cce-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="a5cce-117">**Используются структуры MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="a5cce-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="a5cce-118">Определение раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="a5cce-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="a5cce-119">В идентификаторах записей объектов хранения сообщений и адресной книги для идентификации ответственного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a5cce-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="a5cce-120">В **свойстве PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)сообщений.</span><span class="sxs-lookup"><span data-stu-id="a5cce-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="a5cce-121">Чтобы создать **идентификатор MAPIUID** для ключа поиска, поставщики услуг вызывают [IMAPISupport::NewUID.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="a5cce-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="a5cce-122">Когда клиент передает сообщение по сети, он должен использовать протокол или формат передачи, который не меняет порядок передачи данных **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="a5cce-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="a5cce-123">Дополнительные сведения об используемых **структурах MAPIUID** см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="a5cce-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="a5cce-124">Регистрация уникальных идентификаторов поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="a5cce-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="a5cce-125">Настройка порядка транспорта</span><span class="sxs-lookup"><span data-stu-id="a5cce-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="a5cce-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a5cce-126">See also</span></span>



[<span data-ttu-id="a5cce-127">GUID</span><span class="sxs-lookup"><span data-stu-id="a5cce-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="a5cce-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a5cce-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="a5cce-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="a5cce-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="a5cce-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a5cce-130">MAPI Structures</span></span>](mapi-structures.md)

