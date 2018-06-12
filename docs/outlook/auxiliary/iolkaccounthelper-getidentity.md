---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Получает имя профиля учетной записи.
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807845"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="4ebee-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="4ebee-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="4ebee-104">Получает имя профиля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4ebee-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ebee-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4ebee-105">Quick info</span></span>

<span data-ttu-id="4ebee-106">В разделе [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="4ebee-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="4ebee-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4ebee-107">Parameters</span></span>

<span data-ttu-id="4ebee-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="4ebee-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="4ebee-109">[in] [out] Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="4ebee-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="4ebee-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="4ebee-110">_pcch_</span></span>
  
> <span data-ttu-id="4ebee-111">[in] [out] При вызове этого метода, содержит размер (в символах) _pwszIdentity_ , которая была распределена.</span><span class="sxs-lookup"><span data-stu-id="4ebee-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="4ebee-112">При возврате содержит длину, включая символ, заканчивающийся 0, от имени возвращенные профилей.</span><span class="sxs-lookup"><span data-stu-id="4ebee-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4ebee-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4ebee-113">Return values</span></span>

|<span data-ttu-id="4ebee-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4ebee-114">**HRESULT**</span></span>|<span data-ttu-id="4ebee-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="4ebee-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ebee-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4ebee-116">S_OK</span></span>  <br/> |<span data-ttu-id="4ebee-117">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="4ebee-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="4ebee-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="4ebee-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="4ebee-119">Имя возвращаемых профиля превышает размер _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="4ebee-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="4ebee-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4ebee-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="4ebee-121">_pcch_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4ebee-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ebee-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ebee-122">Remarks</span></span>

<span data-ttu-id="4ebee-123">Если _pwszIdentity_ слишком мал для хранения имени профиля, не будет установлен при возвращении и _pcch_ будет указывать размера для _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="4ebee-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ebee-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4ebee-124">See also</span></span>

- [<span data-ttu-id="4ebee-125">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="4ebee-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="4ebee-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="4ebee-126">PidTagProfileName</span></span>](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

