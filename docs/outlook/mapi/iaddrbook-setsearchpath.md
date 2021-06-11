---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426207"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="ca3be-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ca3be-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="ca3be-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca3be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca3be-105">Задает новый путь поиска в профиле, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="ca3be-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="ca3be-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca3be-106">Parameters</span></span>

 <span data-ttu-id="ca3be-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca3be-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ca3be-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="ca3be-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ca3be-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="ca3be-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="ca3be-110">[in] Указатель на структуру [SRowSet,](srowset.md) используемую для удержания пути поиска.</span><span class="sxs-lookup"><span data-stu-id="ca3be-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="ca3be-111">Первое свойство для каждого **участника aRow**  в **SRowSet** должно быть PR_ENTRYID [(PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ca3be-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca3be-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca3be-112">Return value</span></span>

<span data-ttu-id="ca3be-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca3be-113">S_OK</span></span> 
  
> <span data-ttu-id="ca3be-114">Путь поиска был успешно за установлен.</span><span class="sxs-lookup"><span data-stu-id="ca3be-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="ca3be-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="ca3be-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="ca3be-116">В одном из контейнеров, описанных в **структуре SRowSet,** не было PR_ENTRYID **свойства.**</span><span class="sxs-lookup"><span data-stu-id="ca3be-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ca3be-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca3be-117">Remarks</span></span>

<span data-ttu-id="ca3be-118">Клиенты и поставщики услуг звонят по методу **SetSearchPath,** чтобы сохранить изменения, внесенные в порядок поиска контейнера, который используется для решения имен с помощью [метода IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="ca3be-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="ca3be-119">Путь поиска сохранен между экземплярами сеанса.</span><span class="sxs-lookup"><span data-stu-id="ca3be-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="ca3be-120">Чтобы изменить путь поиска, клиентам и поставщикам не нужно вызывать метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="ca3be-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca3be-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ca3be-121">See also</span></span>



[<span data-ttu-id="ca3be-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ca3be-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="ca3be-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="ca3be-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="ca3be-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ca3be-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="ca3be-125">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="ca3be-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="ca3be-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ca3be-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

