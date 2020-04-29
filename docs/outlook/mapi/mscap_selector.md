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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417205"
---
# <a name="mscap_selector"></a><span data-ttu-id="6b316-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="6b316-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="6b316-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b316-105">Указывает возможности, возвращаемые для хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b316-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6b316-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="6b316-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="6b316-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="6b316-107">Members</span></span>

 <span data-ttu-id="6b316-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="6b316-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="6b316-109">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6b316-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="6b316-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="6b316-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="6b316-111">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6b316-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="6b316-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="6b316-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="6b316-113">Возможности, связанные с вспомогательными папками в магазине.</span><span class="sxs-lookup"><span data-stu-id="6b316-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="6b316-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="6b316-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="6b316-115">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6b316-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="6b316-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="6b316-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="6b316-117">Возможности, связанные с поддержкой ограничений в магазине.</span><span class="sxs-lookup"><span data-stu-id="6b316-117">Capabilities about supporting restrictions on a store.</span></span>
    

