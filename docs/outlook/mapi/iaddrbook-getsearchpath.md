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
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="3bc10-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="3bc10-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="3bc10-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bc10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bc10-105">Возвращает упорядоченный список идентификаторов записей контейнеров, которые необходимо включить в процесс разрешения имен, инициированный методом [IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="3bc10-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="3bc10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bc10-106">Parameters</span></span>

 <span data-ttu-id="3bc10-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3bc10-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3bc10-108">[in] Битоваяmas флагов, которая управляет типом строк, возвращаемого в пути поиска.</span><span class="sxs-lookup"><span data-stu-id="3bc10-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="3bc10-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3bc10-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3bc10-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3bc10-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3bc10-111">Возвращенные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="3bc10-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="3bc10-112">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="3bc10-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3bc10-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="3bc10-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="3bc10-114">[out] Указатель на указатель на упорядоченный список идентификаторов записей контейнера.</span><span class="sxs-lookup"><span data-stu-id="3bc10-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="3bc10-115">**GetSearchPath** сохраняет упорядоченный список в [структуре SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="3bc10-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="3bc10-116">Если в иерархии адресной книги нет контейнеров, в структуре **SRowSet** возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="3bc10-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bc10-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bc10-117">Return value</span></span>

<span data-ttu-id="3bc10-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bc10-118">S_OK</span></span> 
  
> <span data-ttu-id="3bc10-119">Путь поиска был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="3bc10-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bc10-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3bc10-120">Remarks</span></span>

<span data-ttu-id="3bc10-121">Клиенты и поставщики услуг вызвать метод **GetSearchPath,** чтобы получить путь поиска, используемый для разрешения имен с помощью метода **ResolveName.**</span><span class="sxs-lookup"><span data-stu-id="3bc10-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="3bc10-122">Обычно клиенты звонят [методу IAddrBook::SetSearchPath,](iaddrbook-setsearchpath.md) чтобы установить путь поиска контейнера в профиле, прежде чем вызывать **GetSearchPath для** его извлечения.</span><span class="sxs-lookup"><span data-stu-id="3bc10-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="3bc10-123">Однако вызов **SetSearchPath является необязательным.**</span><span class="sxs-lookup"><span data-stu-id="3bc10-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="3bc10-124">Если **SetSearchPath** никогда не был вызван, **GetSearchPath** создает путь, проработав таблицы иерархии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3bc10-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="3bc10-125">Путь поиска по умолчанию, установленный **GetSearchPath,** состоит из следующих контейнеров в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="3bc10-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="3bc10-126">Первый контейнер с разрешением на чтение и записи, обычно это личная адресная книга (PAB).</span><span class="sxs-lookup"><span data-stu-id="3bc10-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="3bc10-127">Каждый контейнер, **для свойства PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)установлено DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="3bc10-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="3bc10-128">Этот параметр указывает, что контейнер содержит получателей.</span><span class="sxs-lookup"><span data-stu-id="3bc10-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="3bc10-129">Контейнер, назначенный в качестве контейнера по умолчанию, если в свойстве  PR_DISPLAY_TYPE нет контейнеров с флагом DT_GLOBAL, а контейнер по умолчанию отличается от первого контейнера с разрешением на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="3bc10-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="3bc10-130">Если **метод SetSearchPath** был вызван, **Метод GetSearchPath** создает путь с помощью контейнеров адресной книги, сохраненных в профиле.</span><span class="sxs-lookup"><span data-stu-id="3bc10-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="3bc10-131">**GetSearchPath** проверяет этот путь, прежде чем возвращать его вызываемой.</span><span class="sxs-lookup"><span data-stu-id="3bc10-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="3bc10-132">После первого вызова **SetSearchPath** последующие вызовы **SetSearchPath** должны использоваться для изменения пути поиска, возвращаемой **GetSearchPath.**</span><span class="sxs-lookup"><span data-stu-id="3bc10-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="3bc10-133">Другими словами, вызываемому клиенту или поставщику не будет назначен путь поиска по умолчанию после первого вызова **SetSearchPath.**</span><span class="sxs-lookup"><span data-stu-id="3bc10-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3bc10-134">См. также</span><span class="sxs-lookup"><span data-stu-id="3bc10-134">See also</span></span>



[<span data-ttu-id="3bc10-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="3bc10-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="3bc10-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="3bc10-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="3bc10-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3bc10-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

