---
title: Использование поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420824"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="5d971-103">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="5d971-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="5d971-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d971-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d971-105">Прежде чем использовать поставщика хранения файлов персональных папок (PST), необходимо инициализировать и настроить поставщика магазина PST.</span><span class="sxs-lookup"><span data-stu-id="5d971-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="5d971-106">После настройки поставщика магазина PST необходимо реализовать функции, чтобы MAPI и spooler MAPI могли войти в систему поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5d971-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="5d971-107">Дополнительные сведения о инициализации и входе в систему поставщика магазина PST см. в инициализации поставщика магазина [PST](initializing-a-wrapped-pst-store-provider.md) и ведения журнала в поставщике упакованных магазинов [PST.](logging-on-to-a-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="5d971-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="5d971-108">Интерфейс **[IMAPISupport::IUnknown](imapisupportiunknown.md)** обеспечивает реализацию задач, которые обычно выполняются поставщиками магазинов сообщений.</span><span class="sxs-lookup"><span data-stu-id="5d971-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="5d971-109">Этот интерфейс должен быть завернут для работы поставщика магазина PST с пакетом образца.</span><span class="sxs-lookup"><span data-stu-id="5d971-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="5d971-110">Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** требует особой реализации.</span><span class="sxs-lookup"><span data-stu-id="5d971-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="5d971-111">Все остальные функции могут передавать свои параметры в завернутый объект.</span><span class="sxs-lookup"><span data-stu-id="5d971-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="5d971-112">В этом разделе функция **IMAPISupport::OpenProfileSection** демонстрируется с помощью примера кода поставщика магазина ПСД sample Wrapped.</span><span class="sxs-lookup"><span data-stu-id="5d971-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="5d971-113">В примере реализован завернутый поставщик PST, который предназначен для использования в сочетании с API репликации.</span><span class="sxs-lookup"><span data-stu-id="5d971-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="5d971-114">Дополнительные сведения о загрузке и установке поставщика магазинов PST sample wrapped см. в примере Установки поставщика упаковки [PST Store.](installing-the-sample-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="5d971-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="5d971-115">Дополнительные сведения об API репликации см. в [иллюстрации API репликации.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="5d971-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="5d971-116">Когда вы закончите использовать поставщика магазина PST, необходимо должным образом закрыть поставщика магазинов PST.</span><span class="sxs-lookup"><span data-stu-id="5d971-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="5d971-117">Дополнительные сведения см. в [переключениях](shutting-down-a-wrapped-pst-store-provider.md)с поставщиком магазина PST.</span><span class="sxs-lookup"><span data-stu-id="5d971-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="5d971-118">Режим раздела "Открытый профиль"</span><span class="sxs-lookup"><span data-stu-id="5d971-118">Open Profile Section routine</span></span>

<span data-ttu-id="5d971-119">Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** открывает раздел текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="5d971-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="5d971-120">Функция требует специальной обработки в реализации поставщика магазина PST.</span><span class="sxs-lookup"><span data-stu-id="5d971-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="5d971-121">При запросе функции возвращается кэшный раздел  `pgNSTGlobalProfileSectionGuid` профиля.</span><span class="sxs-lookup"><span data-stu-id="5d971-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="5d971-122">Пример CSupport::OpenProfileSection()</span><span class="sxs-lookup"><span data-stu-id="5d971-122">CSupport::OpenProfileSection() example</span></span>

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a><span data-ttu-id="5d971-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5d971-123">See also</span></span>

- [<span data-ttu-id="5d971-124">О поставщике пакетных пакетов PST Store</span><span class="sxs-lookup"><span data-stu-id="5d971-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5d971-125">Установка поставщика пакетных пакетов PST</span><span class="sxs-lookup"><span data-stu-id="5d971-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5d971-126">Инициализация поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5d971-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5d971-127">Ведение журнала в поставщике упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5d971-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5d971-128">Отключение поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5d971-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

