---
title: иолкаккаунселпержетидентити
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Получает имя профиля учетной записи.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322108"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="d9442-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="d9442-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="d9442-104">Получает имя профиля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d9442-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9442-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d9442-105">Quick info</span></span>

<span data-ttu-id="d9442-106">Обратитесь к разделу [иолкаккаунселпер](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="d9442-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="d9442-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9442-107">Parameters</span></span>

<span data-ttu-id="d9442-108">_пвсзидентити_</span><span class="sxs-lookup"><span data-stu-id="d9442-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="d9442-109">возврата вышли Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="d9442-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="d9442-110">_пкч_</span><span class="sxs-lookup"><span data-stu-id="d9442-110">_pcch_</span></span>
  
> <span data-ttu-id="d9442-111">возврата вышли При вызове этого метода содержит размер (в знаках) выделенного _пвсзидентити_ .</span><span class="sxs-lookup"><span data-stu-id="d9442-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="d9442-112">После возврата содержит фактическую длину имени возвращаемого профиля, включая 0 — завершающий символ.</span><span class="sxs-lookup"><span data-stu-id="d9442-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d9442-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d9442-113">Return values</span></span>

|<span data-ttu-id="d9442-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d9442-114">**HRESULT**</span></span>|<span data-ttu-id="d9442-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="d9442-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9442-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9442-116">S_OK</span></span>  <br/> |<span data-ttu-id="d9442-117">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="d9442-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="d9442-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d9442-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="d9442-119">Имя возвращаемого профиля превышает размер _пвсзидентити_.</span><span class="sxs-lookup"><span data-stu-id="d9442-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="d9442-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d9442-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="d9442-121">_пкч_ имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="d9442-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9442-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9442-122">Remarks</span></span>

<span data-ttu-id="d9442-123">Если _пвсзидентити_ слишком мал для хранения имени профиля, он не будет установлен для возврата, а _пкч_ будет указывать на размер, необходимый для _пвсзидентити_.</span><span class="sxs-lookup"><span data-stu-id="d9442-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9442-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d9442-124">See also</span></span>

- [<span data-ttu-id="d9442-125">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="d9442-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="d9442-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="d9442-126">PidTagProfileName</span></span>](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

