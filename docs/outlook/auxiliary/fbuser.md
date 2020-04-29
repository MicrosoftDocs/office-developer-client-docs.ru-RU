---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Определяет пользователя, у которого могут быть недоступны данные о занятости.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317663"
---
# <a name="fbuser"></a><span data-ttu-id="56723-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="56723-103">FBUser</span></span>

<span data-ttu-id="56723-104">Определяет пользователя, у которого могут быть недоступны данные о занятости.</span><span class="sxs-lookup"><span data-stu-id="56723-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="56723-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="56723-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="56723-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="56723-106">Members</span></span>

<span data-ttu-id="56723-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="56723-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="56723-108">Длина идентификатора записи пользователя почты, представленного интерфейсом [имаилусер](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) .</span><span class="sxs-lookup"><span data-stu-id="56723-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="56723-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="56723-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="56723-110">Идентификатор элемента почтового пользователя, представленный интерфейсом **имаилусер** .</span><span class="sxs-lookup"><span data-stu-id="56723-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="56723-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="56723-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="56723-112">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="56723-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="56723-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="56723-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="56723-114">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="56723-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56723-115">См. также</span><span class="sxs-lookup"><span data-stu-id="56723-115">See also</span></span>

- [<span data-ttu-id="56723-116">О доступности API</span><span class="sxs-lookup"><span data-stu-id="56723-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="56723-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="56723-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

