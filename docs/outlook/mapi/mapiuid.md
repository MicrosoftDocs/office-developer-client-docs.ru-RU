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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269925"
---
# <a name="mapiuid"></a><span data-ttu-id="0fe9d-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0fe9d-103">MAPIUID</span></span>

  
  
<span data-ttu-id="0fe9d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fe9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fe9d-105">Независимая от порядка байтов версия структуры [GUID](guid.md) , которая используется для уникальной идентификации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fe9d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0fe9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fe9d-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0fe9d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0fe9d-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="0fe9d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="0fe9d-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="0fe9d-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="0fe9d-110">Members</span><span class="sxs-lookup"><span data-stu-id="0fe9d-110">Members</span></span>

 <span data-ttu-id="0fe9d-111">**поисков**</span><span class="sxs-lookup"><span data-stu-id="0fe9d-111">**ab**</span></span>
  
> <span data-ttu-id="0fe9d-112">Массив, содержащий 16 байтового идентификатора.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fe9d-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0fe9d-113">Remarks</span></span>

<span data-ttu-id="0fe9d-114">Структура **мапиуид** — это структура **GUID** , помещенная в последовательность байтов процессора Intel ®.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="0fe9d-115">MAPI создает структуры **мапиуид** таким образом, что два разных элемента могут иметь один и тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="0fe9d-116">Структуры **мапиуид** могут храниться в виде двоичных свойств или файлов, вне зависимости от порядка байтов на компьютере, на котором хранится или осуществляется доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="0fe9d-117">Используются структуры **мапиуид** :</span><span class="sxs-lookup"><span data-stu-id="0fe9d-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="0fe9d-118">Для определения раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="0fe9d-119">В идентификаторах записей хранилища сообщений и объектов адресной книги, чтобы определить поставщика ответственного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="0fe9d-120">В свойстве **пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) messages.</span><span class="sxs-lookup"><span data-stu-id="0fe9d-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="0fe9d-121">Чтобы создать идентификатор **мапиуид** для ключа поиска, поставщики услуг вызывают [Имаписуппорт:: невуид](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="0fe9d-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="0fe9d-122">Когда клиент передает сообщение по сети, он должен использовать протокол или формат передачи, который не изменяет порядок байтов данных **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="0fe9d-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="0fe9d-123">Дополнительные сведения о том, как используются структуры **мапиуид** , приведены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0fe9d-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="0fe9d-124">Регистрация уникальных идентификаторов поставщиков служб</span><span class="sxs-lookup"><span data-stu-id="0fe9d-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="0fe9d-125">Настройка трансПортного заказа</span><span class="sxs-lookup"><span data-stu-id="0fe9d-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="0fe9d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0fe9d-126">See also</span></span>



[<span data-ttu-id="0fe9d-127">GUID</span><span class="sxs-lookup"><span data-stu-id="0fe9d-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="0fe9d-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0fe9d-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="0fe9d-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="0fe9d-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="0fe9d-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="0fe9d-130">MAPI Structures</span></span>](mapi-structures.md)

