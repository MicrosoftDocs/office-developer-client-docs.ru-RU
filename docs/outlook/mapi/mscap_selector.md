---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338677"
---
# <a name="mscapselector"></a><span data-ttu-id="6400e-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="6400e-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="6400e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6400e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6400e-105">Указывает возможности, возвращаемые для хранилища.</span><span class="sxs-lookup"><span data-stu-id="6400e-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6400e-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="6400e-106">Quick info</span></span>

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a><span data-ttu-id="6400e-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="6400e-107">Members</span></span>

 <span data-ttu-id="6400e-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="6400e-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="6400e-109">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6400e-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="6400e-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="6400e-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="6400e-111">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6400e-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="6400e-112">*МСКАП_СЕЛ_ФОЛДЕР*</span><span class="sxs-lookup"><span data-stu-id="6400e-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="6400e-113">Возможности, связанные с вспомогательными папками в магазине.</span><span class="sxs-lookup"><span data-stu-id="6400e-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="6400e-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="6400e-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="6400e-115">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6400e-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="6400e-116">*МСКАП_СЕЛ_РЕСТРИКТИОН*</span><span class="sxs-lookup"><span data-stu-id="6400e-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="6400e-117">Возможности, связанные с поддержкой ограничений в магазине.</span><span class="sxs-lookup"><span data-stu-id="6400e-117">Capabilities about supporting restrictions on a store.</span></span>
    

