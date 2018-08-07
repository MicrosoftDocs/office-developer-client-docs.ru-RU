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
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809917"
---
# <a name="mapiuid"></a><span data-ttu-id="a514a-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a514a-103">MAPIUID</span></span>

  
  
<span data-ttu-id="a514a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a514a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a514a-105">Порядок байтов независимой версия структуру [идентификатор GUID](guid.md) , который используется для уникальной идентификации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a514a-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a514a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a514a-106">Header file:</span></span>  <br/> |<span data-ttu-id="a514a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a514a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a514a-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="a514a-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a514a-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="a514a-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="a514a-110">Members</span><span class="sxs-lookup"><span data-stu-id="a514a-110">Members</span></span>

 <span data-ttu-id="a514a-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="a514a-111">**ab**</span></span>
  
> <span data-ttu-id="a514a-112">Массив, содержащий 16-разрядный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a514a-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a514a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a514a-113">Remarks</span></span>

<span data-ttu-id="a514a-114">Структура **MAPIUID** — это **идентификатор GUID** структура, поместить в байтовом формате Intel® процессора.</span><span class="sxs-lookup"><span data-stu-id="a514a-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="a514a-115">MAPI создает **MAPIUID** структуры, чтобы он очень редко для двух различных элементов требуются тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a514a-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="a514a-116">**MAPIUID** структуры могут храниться как свойства двоичных файлов или файлов, независимо от порядка байтов компьютера, хранения и доступа к сведениям.</span><span class="sxs-lookup"><span data-stu-id="a514a-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="a514a-117">**MAPIUID** структуры используются:</span><span class="sxs-lookup"><span data-stu-id="a514a-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="a514a-118">Для идентификации профиля.</span><span class="sxs-lookup"><span data-stu-id="a514a-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="a514a-119">В операции идентификаторы сообщения хранения и адресной книги объекты для идентификации поставщика услуг ответственность.</span><span class="sxs-lookup"><span data-stu-id="a514a-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="a514a-120">В свойстве **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) сообщений.</span><span class="sxs-lookup"><span data-stu-id="a514a-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="a514a-121">Для создания идентификатор **MAPIUID** для поиска ключ, поставщиков услуг вызвать [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="a514a-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="a514a-122">Если клиент передает сообщения по сети, следует использовать протокол или передачи формат, не изменяйте байтовом **MAPIUID** данных.</span><span class="sxs-lookup"><span data-stu-id="a514a-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="a514a-123">Дополнительные сведения об использовании структур **MAPIUID** в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a514a-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="a514a-124">Регистрация уникальных идентификаторов поставщиков служб</span><span class="sxs-lookup"><span data-stu-id="a514a-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="a514a-125">Установка порядка транспорта</span><span class="sxs-lookup"><span data-stu-id="a514a-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="a514a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a514a-126">See also</span></span>



[<span data-ttu-id="a514a-127">GUID</span><span class="sxs-lookup"><span data-stu-id="a514a-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="a514a-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a514a-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="a514a-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="a514a-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="a514a-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a514a-130">MAPI Structures</span></span>](mapi-structures.md)

