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
ms.openlocfilehash: a6eba20fb346f53052808abf8fcae8993d423d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589562"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="162aa-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="162aa-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="162aa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="162aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="162aa-105">Рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="162aa-105">Deprecated.</span></span> <span data-ttu-id="162aa-106">Назначает новое имя службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="162aa-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="162aa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="162aa-107">Parameters</span></span>

 <span data-ttu-id="162aa-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="162aa-108">_lpUID_</span></span>
  
> <span data-ttu-id="162aa-109">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений переименовать.</span><span class="sxs-lookup"><span data-stu-id="162aa-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="162aa-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="162aa-110">_ulFlags_</span></span>
  
> <span data-ttu-id="162aa-111">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="162aa-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="162aa-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="162aa-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="162aa-113">[in] Указатель на новое имя для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="162aa-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="162aa-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="162aa-114">Return value</span></span>

<span data-ttu-id="162aa-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="162aa-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="162aa-116">MAPI не поддерживает переименование этой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="162aa-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="162aa-117">**RenameMsgService** всегда возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="162aa-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="162aa-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="162aa-118">Remarks</span></span>

<span data-ttu-id="162aa-119">Чтобы назначить новое имя службы сообщений, клиенты следует использовать свойство **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="162aa-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="162aa-120">Имена поставщиков услуг службы сообщений сохраняются в их свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="162aa-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="162aa-121">См. также</span><span class="sxs-lookup"><span data-stu-id="162aa-121">See also</span></span>



[<span data-ttu-id="162aa-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="162aa-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="162aa-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="162aa-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

