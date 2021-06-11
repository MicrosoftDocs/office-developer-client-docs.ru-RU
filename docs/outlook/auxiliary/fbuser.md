---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Определяет пользователя, у которого могут быть свободные или загруженные данные.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317663"
---
# <a name="fbuser"></a><span data-ttu-id="ecb6f-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="ecb6f-103">FBUser</span></span>

<span data-ttu-id="ecb6f-104">Определяет пользователя, у которого могут быть свободные или загруженные данные.</span><span class="sxs-lookup"><span data-stu-id="ecb6f-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ecb6f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ecb6f-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="ecb6f-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="ecb6f-106">Members</span></span>

<span data-ttu-id="ecb6f-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="ecb6f-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="ecb6f-108">Длина ID записи пользователя почты, представленного [интерфейсом IMailUser.](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)</span><span class="sxs-lookup"><span data-stu-id="ecb6f-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="ecb6f-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="ecb6f-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="ecb6f-110">ID записи пользователя почты, представленный **интерфейсом IMailUser.**</span><span class="sxs-lookup"><span data-stu-id="ecb6f-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="ecb6f-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="ecb6f-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="ecb6f-112">Этот параметр зарезервирован для Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ecb6f-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="ecb6f-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="ecb6f-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="ecb6f-114">Этот параметр зарезервирован для Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ecb6f-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecb6f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ecb6f-115">See also</span></span>

- [<span data-ttu-id="ecb6f-116">О доступности API</span><span class="sxs-lookup"><span data-stu-id="ecb6f-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="ecb6f-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="ecb6f-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

