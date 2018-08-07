---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812573"
---
# <a name="upreade"></a><span data-ttu-id="b7f85-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="b7f85-103">UPREADE</span></span>

<span data-ttu-id="b7f85-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7f85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7f85-105">Расширенные сведения для загрузки состояние чтения элемента во время [Отправить прочитать состояние состояние](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="b7f85-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b7f85-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b7f85-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="b7f85-107">Members</span><span class="sxs-lookup"><span data-stu-id="b7f85-107">Members</span></span>

<span data-ttu-id="b7f85-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7f85-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="b7f85-109">[out] и [in] флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="b7f85-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="b7f85-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="b7f85-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="b7f85-111">[out] Элемент скрыт.</span><span class="sxs-lookup"><span data-stu-id="b7f85-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="b7f85-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="b7f85-112">UPR_READ</span></span>
    
    - <span data-ttu-id="b7f85-113">[out] Изменилось состояние чтения элемента.</span><span class="sxs-lookup"><span data-stu-id="b7f85-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="b7f85-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="b7f85-114">UPR_OK</span></span>
    
    - <span data-ttu-id="b7f85-115">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="b7f85-115">[in] Upload was successful.</span></span> <span data-ttu-id="b7f85-116">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="b7f85-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="b7f85-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b7f85-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="b7f85-118">[in] Отправьте состояние чтения элемента сейчас, вместо ожидания до конца [Отправить состояние таблицы](upload-table-state.md) для пакетной обработки более одного элемента.</span><span class="sxs-lookup"><span data-stu-id="b7f85-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="b7f85-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="b7f85-119">_skey_</span></span>
  
> <span data-ttu-id="b7f85-120">[out] Ключ исходного элемента.</span><span class="sxs-lookup"><span data-stu-id="b7f85-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7f85-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b7f85-121">See also</span></span>

- [<span data-ttu-id="b7f85-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="b7f85-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b7f85-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="b7f85-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b7f85-124">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="b7f85-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="b7f85-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="b7f85-125">UPREAD</span></span>](upread.md)

