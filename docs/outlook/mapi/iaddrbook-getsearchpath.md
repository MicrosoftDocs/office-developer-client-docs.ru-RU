---
title: Иаддрбукжетсеарчпас
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341393"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="9c926-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9c926-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="9c926-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c926-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c926-105">Возвращает упорядоченный список идентификаторов элементов контейнеров, которые должны быть включены в процесс разрешения имен, инициированный методом [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="9c926-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="9c926-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c926-106">Parameters</span></span>

 <span data-ttu-id="9c926-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c926-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9c926-108">возврата Битовая маска флагов, определяющая тип строк, возвращаемых в пути поиска.</span><span class="sxs-lookup"><span data-stu-id="9c926-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="9c926-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9c926-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9c926-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c926-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9c926-111">Возвращаемые строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="9c926-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="9c926-112">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9c926-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9c926-113">_Лппсеарчпас_</span><span class="sxs-lookup"><span data-stu-id="9c926-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="9c926-114">вышли Указатель на указатель на упорядоченный список идентификаторов записей контейнера.</span><span class="sxs-lookup"><span data-stu-id="9c926-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="9c926-115">**Жетсеарчпас** сохраняет упорядоченный список в структуре [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="9c926-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="9c926-116">Если в иерархии адресной книги нет контейнеров, в структуре **SRowSet** возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="9c926-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9c926-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c926-117">Return value</span></span>

<span data-ttu-id="9c926-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c926-118">S_OK</span></span> 
  
> <span data-ttu-id="9c926-119">Путь поиска успешно получен.</span><span class="sxs-lookup"><span data-stu-id="9c926-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c926-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c926-120">Remarks</span></span>

<span data-ttu-id="9c926-121">Клиенты и поставщики услуг вызывают метод **жетсеарчпас** , чтобы получить путь поиска, используемый для разрешения имен с помощью метода **ресолвенаме** .</span><span class="sxs-lookup"><span data-stu-id="9c926-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="9c926-122">Как правило, клиенты вызывают метод [IAddrBook:: сетсеарчпас](iaddrbook-setsearchpath.md) для установки пути поиска контейнера в профиле перед вызовом **жетсеарчпас** для их извлечения.</span><span class="sxs-lookup"><span data-stu-id="9c926-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="9c926-123">Однако вызывать **сетсеарчпас** необязательно.</span><span class="sxs-lookup"><span data-stu-id="9c926-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="9c926-124">Если **сетсеарчпас** никогда не вызывался, **жетсеарчпас** создает путь, работая через таблицы иерархий адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9c926-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="9c926-125">Путь поиска по умолчанию, устанавливаемый **жетсеарчпас** , состоит из следующих контейнеров в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="9c926-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="9c926-126">Первый контейнер с разрешениями на чтение и запись, обычно это личная адресная книга (PAB).</span><span class="sxs-lookup"><span data-stu-id="9c926-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="9c926-127">Для каждого контейнера, у которого свойство **пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) задано значение дт_глобал.</span><span class="sxs-lookup"><span data-stu-id="9c926-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="9c926-128">Этот параметр указывает на то, что контейнер содержит получателей.</span><span class="sxs-lookup"><span data-stu-id="9c926-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="9c926-129">Контейнер, назначенный по умолчанию, если в свойстве **пр_дисплай_типе** нет контейнеров с установленным флагом дт_глобал, а контейнер по умолчанию отличается от первого контейнера с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="9c926-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="9c926-130">При вызове **Сетсеарчпас** **жетсеарчпас** создает путь с помощью контейнеров адресной книги, которые хранились в профиле.</span><span class="sxs-lookup"><span data-stu-id="9c926-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="9c926-131">**Жетсеарчпас** проверяет этот путь перед возвращением в вызывающий абонент.</span><span class="sxs-lookup"><span data-stu-id="9c926-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="9c926-132">После первого вызова **сетсеарчпас**последующие вызовы **сетсеарчпас** необходимо использовать для изменения пути поиска, возвращаемого **жетсеарчпас**.</span><span class="sxs-lookup"><span data-stu-id="9c926-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="9c926-133">Другими словами, вызывающий клиент или поставщик не получают путь поиска по умолчанию после первого вызова в **сетсеарчпас**.</span><span class="sxs-lookup"><span data-stu-id="9c926-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c926-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9c926-134">See also</span></span>



[<span data-ttu-id="9c926-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9c926-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="9c926-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9c926-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="9c926-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9c926-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

