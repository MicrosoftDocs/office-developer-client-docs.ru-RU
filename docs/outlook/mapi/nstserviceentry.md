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
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280056"
---
# <a name="nstserviceentry"></a><span data-ttu-id="a6926-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="a6926-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="a6926-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6926-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6926-105">Функция точки входа службы сообщений для поставщика точки входа MAPI для переноса локального магазина на основе PST в NST-хранилище.</span><span class="sxs-lookup"><span data-stu-id="a6926-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a6926-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a6926-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6926-107">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a6926-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6926-108">Поставщик MAPI</span><span class="sxs-lookup"><span data-stu-id="a6926-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="a6926-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a6926-109">Called by:</span></span>  <br/> |<span data-ttu-id="a6926-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a6926-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a6926-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6926-111">Parameters</span></span>

 <span data-ttu-id="a6926-112">**NSTServiceEntry использует** прототип **[функции MSGSERVICEENTRY.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a6926-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="a6926-113">Сведения о его параметрах см. в **[msGSERVICEENTRY.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a6926-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="a6926-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a6926-114">Return values</span></span>

<span data-ttu-id="a6926-115">Сведения о возвращаемом значении см. в **[msGSERVICEENTRY.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a6926-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6926-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6926-116">Remarks</span></span>

<span data-ttu-id="a6926-117">При использовании **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** для искомого адреса этой функции в msmapi32.dll укажите "NSTServiceEntry" в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="a6926-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="a6926-118">Чтобы использовать API репликации, поставщик магазина MAPI должен сначала открыть и завернуть локальное хранилище на основе PST, вызывая **[NSTServiceEntry.](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a6926-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="a6926-119">Затем поставщик может использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)** для выполнения репликации.</span><span class="sxs-lookup"><span data-stu-id="a6926-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="a6926-120">К NST- магазину применяются следующие замечания:</span><span class="sxs-lookup"><span data-stu-id="a6926-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="a6926-121">Не храните информацию в разделе глобального профиля при реализации поставщика MAPI, который использует **NSTServiceEntry.**</span><span class="sxs-lookup"><span data-stu-id="a6926-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="a6926-122">Раздел глобального профиля совместно с другими поставщиками, и данные, хранимые в этом профиле, могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="a6926-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="a6926-123">Только элементы с существующими отметками времени изменения обновляют свои отметки при их экономии.</span><span class="sxs-lookup"><span data-stu-id="a6926-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="a6926-124">При сэкономлении элементов проверка конфликтов не происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="a6926-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="a6926-125">Повторяющиеся обнаружения не происходят при экономии элементов.</span><span class="sxs-lookup"><span data-stu-id="a6926-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="a6926-126">Файл, представляющий кэшную версию сервера, будет к ним придан. NST.</span><span class="sxs-lookup"><span data-stu-id="a6926-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="a6926-127">Чтобы получить указатель на глобальный раздел профиля, служба сообщений вызывает **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** в объекте поддержки с помощью **pbNSTGlobalProfileSectionGuid,** как определено ниже:</span><span class="sxs-lookup"><span data-stu-id="a6926-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="a6926-128">В этом случае объект поддержки службы сообщений должен гарантировать, что **IMAPISupport::OpenProfileSection** возвращает раздел профиля, который определен свойством **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** в разделе профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6926-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="a6926-129">Чтобы получить этот раздел профиля, объект поддержки может открыть раздел профиля по умолчанию, извлечь PR_SERVICE_UID и передать результат **в IMAPISupport::OpenProfileSection,** чтобы получить правильный раздел глобального профиля.</span><span class="sxs-lookup"><span data-stu-id="a6926-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="a6926-130">Объект поддержки, в свою очередь, возвращает указатель на этот раздел глобального профиля службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="a6926-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a6926-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a6926-131">See also</span></span>



[<span data-ttu-id="a6926-132">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="a6926-132">About the Replication API</span></span>](about-the-replication-api.md)

