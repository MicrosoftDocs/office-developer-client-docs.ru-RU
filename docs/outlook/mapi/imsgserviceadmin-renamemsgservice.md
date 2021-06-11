---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422105"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="6cc92-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="6cc92-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="6cc92-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cc92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cc92-105">Устарело.</span><span class="sxs-lookup"><span data-stu-id="6cc92-105">Deprecated.</span></span> <span data-ttu-id="6cc92-106">Назначает новое имя службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cc92-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="6cc92-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6cc92-107">Parameters</span></span>

 <span data-ttu-id="6cc92-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="6cc92-108">_lpUID_</span></span>
  
> <span data-ttu-id="6cc92-109">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений для переименования.</span><span class="sxs-lookup"><span data-stu-id="6cc92-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="6cc92-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6cc92-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6cc92-111">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="6cc92-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6cc92-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="6cc92-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="6cc92-113">[in] Указатель на новое имя службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cc92-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6cc92-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cc92-114">Return value</span></span>

<span data-ttu-id="6cc92-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6cc92-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6cc92-116">MAPI не поддерживает переименование этой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cc92-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="6cc92-117">**ПереименованиеMsgService** всегда возвращает это значение.</span><span class="sxs-lookup"><span data-stu-id="6cc92-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6cc92-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="6cc92-118">Remarks</span></span>

<span data-ttu-id="6cc92-119">Чтобы назначить новое имя службе сообщений, клиенты должны использовать **свойство** [PR_SERVICE_NAME (PidTagServiceName)](pidtagservicename-canonical-property.md)службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cc92-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="6cc92-120">Имена поставщиков услуг в службе сообщений хранятся в **свойствах PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6cc92-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6cc92-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6cc92-121">See also</span></span>



[<span data-ttu-id="6cc92-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6cc92-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6cc92-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6cc92-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

