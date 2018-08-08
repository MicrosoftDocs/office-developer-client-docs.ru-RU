---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810043"
---
# <a name="nstserviceentry"></a><span data-ttu-id="91d7b-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="91d7b-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="91d7b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91d7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91d7b-105">Поставщик для упаковки в локальном хранилище на основе PST-файлов в качестве хранилище NST хранилища сообщений службы функцию точки входа для MAPI.</span><span class="sxs-lookup"><span data-stu-id="91d7b-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="91d7b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="91d7b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91d7b-107">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="91d7b-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="91d7b-108">Поставщик MAPI</span><span class="sxs-lookup"><span data-stu-id="91d7b-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="91d7b-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="91d7b-109">Called by:</span></span>  <br/> |<span data-ttu-id="91d7b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="91d7b-110">MAPI</span></span>  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a><span data-ttu-id="91d7b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="91d7b-111">Parameters</span></span>

 <span data-ttu-id="91d7b-112">**NSTServiceEntry** использует прототип функции **[MSGSERVICEENTRY](msgserviceentry.md)** .</span><span class="sxs-lookup"><span data-stu-id="91d7b-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="91d7b-113">Сведения о его параметров содержатся **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="91d7b-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="91d7b-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="91d7b-114">Return values</span></span>

<span data-ttu-id="91d7b-115">Возвращаемые значения содержатся в разделе **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="91d7b-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="91d7b-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="91d7b-116">Remarks</span></span>

<span data-ttu-id="91d7b-117">При использовании **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** следует искать адреса этой функции msmapi32.dll, укажите «NSTServiceEntry» в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="91d7b-117">When using **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="91d7b-118">Чтобы использовать API репликации, поставщик хранилища MAPI сначала необходимо открыть и перенос локального хранилища на основе PST-файлов, вызвав **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="91d7b-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="91d7b-119">Поставщик затем можно использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)**, чтобы выполнить репликацию.</span><span class="sxs-lookup"><span data-stu-id="91d7b-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="91d7b-120">Следующие вычисляются в хранилище NST:</span><span class="sxs-lookup"><span data-stu-id="91d7b-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="91d7b-121">Не следует хранить какие-либо сведения в разделе глобальные профиля, при реализации поставщика MAPI, который использует **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="91d7b-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="91d7b-122">В разделе глобальные профилей совместно используемой многие поставщики и данных, хранящихся в этот профиль может быть перезаписана.</span><span class="sxs-lookup"><span data-stu-id="91d7b-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="91d7b-123">Только элементы с существующей отметки времени изменения получите их пометок обновлены при сохранении.</span><span class="sxs-lookup"><span data-stu-id="91d7b-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="91d7b-124">Проверка конфликтов не происходит автоматически при сохранении элементов.</span><span class="sxs-lookup"><span data-stu-id="91d7b-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="91d7b-125">Поиск повторяющихся данных не происходит при сохранении элементов.</span><span class="sxs-lookup"><span data-stu-id="91d7b-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="91d7b-126">Добавляется файл, представляющий кэшированная версия сервера. NST.</span><span class="sxs-lookup"><span data-stu-id="91d7b-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="91d7b-127">Для получения указатель в разделе глобальные профилей, служба сообщений вызывает **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** в объекте поддержки с помощью **pbNSTGlobalProfileSectionGuid** , как указано ниже:</span><span class="sxs-lookup"><span data-stu-id="91d7b-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="91d7b-128">В этом случае объект поддержки службы сообщений следует убедиться, что **IMAPISupport::OpenProfileSection** возвращает раздела профиля, который идентифицируется свойством **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** в разделе профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91d7b-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="91d7b-129">Для получения в этом разделе профилей, объект поддержки можно откройте раздел профиля по умолчанию, получить **PR_SERVICE_UID**и передать результат в **IMAPISupport::OpenProfileSection** для получения раздела правильные глобальные профиля.</span><span class="sxs-lookup"><span data-stu-id="91d7b-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="91d7b-130">Объект поддержки в свою очередь возвращает указатель на в этом разделе глобального профиля для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="91d7b-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="91d7b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="91d7b-131">See also</span></span>



[<span data-ttu-id="91d7b-132">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="91d7b-132">About the Replication API</span></span>](about-the-replication-api.md)

