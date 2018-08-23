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
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588127"
---
# <a name="mscapselector"></a><span data-ttu-id="7b582-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="7b582-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="7b582-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b582-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b582-105">Задает возможности, чтобы возвратить хранилища.</span><span class="sxs-lookup"><span data-stu-id="7b582-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7b582-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7b582-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7b582-107">Members</span><span class="sxs-lookup"><span data-stu-id="7b582-107">Members</span></span>

 <span data-ttu-id="7b582-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="7b582-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="7b582-109">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b582-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="7b582-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="7b582-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="7b582-111">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b582-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="7b582-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="7b582-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="7b582-113">Возможности о вспомогательных папок для хранилища.</span><span class="sxs-lookup"><span data-stu-id="7b582-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="7b582-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="7b582-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="7b582-115">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b582-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="7b582-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="7b582-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="7b582-117">Возможности о поддержке ограничения для хранилища.</span><span class="sxs-lookup"><span data-stu-id="7b582-117">Capabilities about supporting restrictions on a store.</span></span>
    

