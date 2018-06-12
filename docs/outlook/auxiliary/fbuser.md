---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Идентифицирует пользователя, который может не иметь сведений о доступности данных, которые доступны.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807684"
---
# <a name="fbuser"></a><span data-ttu-id="30b5c-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="30b5c-103">FBUser</span></span>

<span data-ttu-id="30b5c-104">Идентифицирует пользователя, который может не иметь сведений о доступности данных, которые доступны.</span><span class="sxs-lookup"><span data-stu-id="30b5c-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30b5c-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="30b5c-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="30b5c-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="30b5c-106">Members</span></span>

<span data-ttu-id="30b5c-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="30b5c-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="30b5c-108">Длина записи идентификатор пользователя почты, представленных в интерфейсе [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30b5c-108">The length of the entry ID of the mail user as represented by the [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) interface.</span></span> 
    
<span data-ttu-id="30b5c-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="30b5c-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="30b5c-110">Идентификатор записи пользователя почты, представленных в интерфейсе **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="30b5c-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="30b5c-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="30b5c-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="30b5c-112">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30b5c-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="30b5c-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="30b5c-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="30b5c-114">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30b5c-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30b5c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="30b5c-115">See also</span></span>

- [<span data-ttu-id="30b5c-116">About the Free/Busy API</span><span class="sxs-lookup"><span data-stu-id="30b5c-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="30b5c-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="30b5c-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

