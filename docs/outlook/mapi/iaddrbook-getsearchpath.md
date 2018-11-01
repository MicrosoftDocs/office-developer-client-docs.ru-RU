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
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580700"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="6df91-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="6df91-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="6df91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6df91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6df91-105">Возвращает упорядоченный список идентификаторов запись контейнеров, которые будут включены в процесс разрешения имен, которые запускаются с помощью метода [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="6df91-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="6df91-106">���������</span><span class="sxs-lookup"><span data-stu-id="6df91-106">Parameters</span></span>

 <span data-ttu-id="6df91-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6df91-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6df91-108">[in] Битовая маска флаги, определяющее тип строк, возвращаемых в путь поиска.</span><span class="sxs-lookup"><span data-stu-id="6df91-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="6df91-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6df91-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6df91-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6df91-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6df91-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="6df91-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="6df91-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6df91-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6df91-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="6df91-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="6df91-114">[out] Указатель на указатель упорядоченный список идентификаторов запись контейнера.</span><span class="sxs-lookup"><span data-stu-id="6df91-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="6df91-115">**GetSearchPath** сохранение упорядоченный список в структуре [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="6df91-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="6df91-116">Если в иерархии адресной книги не контейнеров, возвращается ноль в структуре **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="6df91-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6df91-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6df91-117">Return value</span></span>

<span data-ttu-id="6df91-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6df91-118">S_OK</span></span> 
  
> <span data-ttu-id="6df91-119">Путь поиска был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="6df91-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6df91-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="6df91-120">Remarks</span></span>

<span data-ttu-id="6df91-121">Клиенты и поставщики услуг вызовите метод **GetSearchPath** для получения пути поиска, который используется для разрешения имен с помощью метода **ResolveName** .</span><span class="sxs-lookup"><span data-stu-id="6df91-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="6df91-122">Как правило клиенты вызовите метод [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) для установления путь поиска контейнера в профиле перед звонят **GetSearchPath** для его извлечения.</span><span class="sxs-lookup"><span data-stu-id="6df91-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="6df91-123">Тем не менее вызов **SetSearchPath** не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6df91-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="6df91-124">Если **SetSearchPath** никогда не был вызван, **GetSearchPath** строится путь с выполнением адрес таблиц иерархии книги.</span><span class="sxs-lookup"><span data-stu-id="6df91-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="6df91-125">Путь поиска по умолчанию, установленные **GetSearchPath** состоит из следующих контейнеров в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="6df91-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="6df91-126">Первый контейнер, получившие разрешение на чтение и запись, обычно Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="6df91-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="6df91-127">Каждый контейнер, задайте значение DT_GLOBAL свойства **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6df91-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="6df91-128">Этот параметр указывает, что в контейнере получателей.</span><span class="sxs-lookup"><span data-stu-id="6df91-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="6df91-129">Контейнер, назначенный по умолчанию, если нет контейнеров, имеющие флаг DT_GLOBAL в их свойство **PR_DISPLAY_TYPE** и контейнер по умолчанию отличается от первого контейнера получившие разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="6df91-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="6df91-130">При вызове **SetSearchPath** **GetSearchPath** создает путь с помощью контейнеров адресной книги, сохраненные в профиле.</span><span class="sxs-lookup"><span data-stu-id="6df91-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="6df91-131">**GetSearchPath** проверяет этот путь до его возврата вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="6df91-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="6df91-132">После первого вызова **SetSearchPath**последующие вызовы **SetSearchPath** должен использоваться для изменения пути поиска, возвращаемые **GetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="6df91-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="6df91-133">Другими словами вызывающей клиента или поставщика не получает путь поиска по умолчанию после первого вызова **SetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="6df91-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6df91-134">См. также</span><span class="sxs-lookup"><span data-stu-id="6df91-134">See also</span></span>



[<span data-ttu-id="6df91-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="6df91-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="6df91-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="6df91-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="6df91-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6df91-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

