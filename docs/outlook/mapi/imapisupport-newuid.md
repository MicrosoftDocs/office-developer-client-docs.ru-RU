---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 244087c41e33e470c42434e9d57cee7317bcb78c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571691"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="09db5-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="09db5-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="09db5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09db5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09db5-105">Создает новую структуру [MAPIUID](mapiuid.md) для использования в качестве уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="09db5-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="09db5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09db5-106">Parameters</span></span>

 <span data-ttu-id="09db5-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="09db5-107">_lpMuid_</span></span>
  
> <span data-ttu-id="09db5-108">Указатель на структуру нового **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="09db5-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09db5-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="09db5-109">Return value</span></span>

<span data-ttu-id="09db5-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="09db5-110">S_OK</span></span> 
  
> <span data-ttu-id="09db5-111">Был создан новый структуры **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="09db5-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09db5-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="09db5-112">Remarks</span></span>

<span data-ttu-id="09db5-113">Метод **IMAPISupport::NewUID** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="09db5-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="09db5-114">Поставщики службы и службы сообщений вызов **NewUID** каждый раз, когда они должны получать долгосрочного уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="09db5-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="09db5-115">Сообщение хранилища поставщика, например, можно вызвать метод **NewUID** для получения **MAPIUID** для помещения в свойство **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) только что созданный сообщения.</span><span class="sxs-lookup"><span data-stu-id="09db5-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="09db5-116">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="09db5-116">Notes to callers</span></span>

<span data-ttu-id="09db5-117">Не следует путать структуру **MAPIUID** , зарегистрируйте во время входа в систему с помощью структуры **MAPIUID** , метод **NewUID** создает.</span><span class="sxs-lookup"><span data-stu-id="09db5-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="09db5-118">Структура **MAPIUID** , зарегистрируйте при вызове метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) представляет адресной книги или сообщение хранения поставщика MAPI и используется для различения идентификаторы записей, создаваемых различных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="09db5-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="09db5-119">Эта структура **MAPIUID** следует жестко и не получить путем вызова **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="09db5-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09db5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="09db5-120">See also</span></span>



[<span data-ttu-id="09db5-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="09db5-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="09db5-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="09db5-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

