---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412984"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="4e818-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="4e818-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="4e818-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e818-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e818-105">Возвращает упорядоченный список идентификаторов входных контейнеров, которые будут включены в процесс разрешения имен, инициированный методом [IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="4e818-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="4e818-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e818-106">Parameters</span></span>

 <span data-ttu-id="4e818-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e818-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4e818-108">[in] Немного флагов, которые контролируют тип строк, возвращаемых в пути поиска.</span><span class="sxs-lookup"><span data-stu-id="4e818-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="4e818-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4e818-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4e818-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4e818-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4e818-111">Возвращенные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="4e818-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="4e818-112">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4e818-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="4e818-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="4e818-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="4e818-114">[вышел] Указатель на указатель на упорядоченный список идентификаторов записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="4e818-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="4e818-115">**GetSearchPath** сохраняет упорядоченный список в [структуре SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="4e818-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="4e818-116">Если в иерархии адресных книг нет контейнеров, в структуре **SRowSet** возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="4e818-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e818-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e818-117">Return value</span></span>

<span data-ttu-id="4e818-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e818-118">S_OK</span></span> 
  
> <span data-ttu-id="4e818-119">Путь поиска был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="4e818-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e818-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e818-120">Remarks</span></span>

<span data-ttu-id="4e818-121">Клиенты и поставщики услуг звонят по **методу GetSearchPath,** чтобы получить путь поиска, используемый для решения имен с помощью **метода ResolveName.**</span><span class="sxs-lookup"><span data-stu-id="4e818-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="4e818-122">Как правило, клиенты звонят по методу [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) для создания пути поиска контейнеров в профиле, прежде чем вызывать **GetSearchPath** для его получения.</span><span class="sxs-lookup"><span data-stu-id="4e818-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="4e818-123">Однако вызов **SetSearchPath** необязателен.</span><span class="sxs-lookup"><span data-stu-id="4e818-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="4e818-124">Если **SetSearchPath** никогда не назывался, **GetSearchPath** создает путь, проработав таблицы иерархии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4e818-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="4e818-125">Путь поиска по умолчанию, установленный **GetSearchPath,** состоит из следующих контейнеров в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="4e818-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="4e818-126">Первый контейнер с разрешением на чтение и написание, как правило, личный адрес (PAB).</span><span class="sxs-lookup"><span data-stu-id="4e818-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="4e818-127">Каждый контейнер с **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)имеет свойство DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="4e818-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="4e818-128">Этот параметр указывает, что контейнер содержит получателей.</span><span class="sxs-lookup"><span data-stu-id="4e818-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="4e818-129">Контейнер, назначенный по умолчанию, если в свойстве PR_DISPLAY_TYPE установлен флаг DT_GLOBAL, а контейнер по умолчанию отличается от первого контейнера разрешением на чтение и записи. </span><span class="sxs-lookup"><span data-stu-id="4e818-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="4e818-130">Если **setSearchPath** был вызван, **GetSearchPath** создает путь с помощью контейнеров адресной книги, хранимых в профиле.</span><span class="sxs-lookup"><span data-stu-id="4e818-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="4e818-131">**GetSearchPath** проверяет этот путь, прежде чем он возвращает его вызываемой.</span><span class="sxs-lookup"><span data-stu-id="4e818-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="4e818-132">После первого вызова **в SetSearchPath** необходимо использовать последующие вызовы **в SetSearchPath** для изменения пути поиска, возвращенного **GetSearchPath.**</span><span class="sxs-lookup"><span data-stu-id="4e818-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="4e818-133">Другими словами, клиент или поставщик вызовов не получает путь поиска по умолчанию после первого вызова **в SetSearchPath.**</span><span class="sxs-lookup"><span data-stu-id="4e818-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e818-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4e818-134">See also</span></span>



[<span data-ttu-id="4e818-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="4e818-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="4e818-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="4e818-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="4e818-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4e818-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

