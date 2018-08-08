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
ms.openlocfilehash: 4f9d2f4d271e467d8fac32b8f17faa8f66cd3f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808772"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="81e05-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="81e05-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="81e05-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81e05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81e05-105">Задает новый путь для поиска профиля, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="81e05-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="81e05-106">���������</span><span class="sxs-lookup"><span data-stu-id="81e05-106">Parameters</span></span>

 <span data-ttu-id="81e05-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81e05-107">_ulFlags_</span></span>
  
> <span data-ttu-id="81e05-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="81e05-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="81e05-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="81e05-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="81e05-110">[in] Указатель на структуру [SRowSet](srowset.md) , используемый для хранения путь поиска.</span><span class="sxs-lookup"><span data-stu-id="81e05-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="81e05-111">Первое свойство для каждого элемента **aRow** в **SRowSet** должно быть **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81e05-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81e05-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="81e05-112">Return value</span></span>

<span data-ttu-id="81e05-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="81e05-113">S_OK</span></span> 
  
> <span data-ttu-id="81e05-114">Путь поиска успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="81e05-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="81e05-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="81e05-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="81e05-116">Один из контейнеров, описанного в структуре **SRowSet** не содержит свойство **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="81e05-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="81e05-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="81e05-117">Remarks</span></span>

<span data-ttu-id="81e05-118">Клиенты и поставщиков услуг вызовите метод **SetSearchPath** , чтобы сохранить изменения, внесенные в порядке поиска контейнер, используемый для разрешения имен с помощью метода [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="81e05-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="81e05-119">Путь поиска сохраняется между экземплярами сеанса.</span><span class="sxs-lookup"><span data-stu-id="81e05-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="81e05-120">Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для вступления изменений в путь поиска было постоянным.</span><span class="sxs-lookup"><span data-stu-id="81e05-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81e05-121">См. также</span><span class="sxs-lookup"><span data-stu-id="81e05-121">See also</span></span>



[<span data-ttu-id="81e05-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="81e05-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="81e05-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="81e05-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="81e05-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="81e05-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="81e05-125">Каноническое свойство PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="81e05-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="81e05-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="81e05-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

