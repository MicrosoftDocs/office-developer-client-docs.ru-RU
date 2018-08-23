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
ms.openlocfilehash: 1d486344ab20ef49488dbb911f3dd7000d64942e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571761"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="f104c-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="f104c-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="f104c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f104c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f104c-105">Задает новый путь для поиска профиля, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="f104c-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="f104c-106">���������</span><span class="sxs-lookup"><span data-stu-id="f104c-106">Parameters</span></span>

 <span data-ttu-id="f104c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f104c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f104c-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f104c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f104c-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="f104c-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="f104c-110">[in] Указатель на структуру [SRowSet](srowset.md) , используемый для хранения путь поиска.</span><span class="sxs-lookup"><span data-stu-id="f104c-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="f104c-111">Первое свойство для каждого элемента **aRow** в **SRowSet** должно быть **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f104c-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f104c-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f104c-112">Return value</span></span>

<span data-ttu-id="f104c-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f104c-113">S_OK</span></span> 
  
> <span data-ttu-id="f104c-114">Путь поиска успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="f104c-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="f104c-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="f104c-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="f104c-116">Один из контейнеров, описанного в структуре **SRowSet** не содержит свойство **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="f104c-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f104c-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="f104c-117">Remarks</span></span>

<span data-ttu-id="f104c-118">Клиенты и поставщиков услуг вызовите метод **SetSearchPath** , чтобы сохранить изменения, внесенные в порядке поиска контейнер, используемый для разрешения имен с помощью метода [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="f104c-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="f104c-119">Путь поиска сохраняется между экземплярами сеанса.</span><span class="sxs-lookup"><span data-stu-id="f104c-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="f104c-120">Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для вступления изменений в путь поиска было постоянным.</span><span class="sxs-lookup"><span data-stu-id="f104c-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f104c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f104c-121">See also</span></span>



[<span data-ttu-id="f104c-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="f104c-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="f104c-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="f104c-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="f104c-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="f104c-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="f104c-125">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="f104c-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="f104c-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f104c-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

