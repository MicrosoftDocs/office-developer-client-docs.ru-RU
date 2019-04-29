---
title: Использование поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Дата последнего изменения: 03 июля, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420824"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="f92ee-103">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="f92ee-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="f92ee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f92ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f92ee-105">Перед использованием упакованного поставщика хранилища файлов личных папок (PST) необходимо инициализировать и настроить поставщик упакованного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="f92ee-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="f92ee-106">После настройки поставщика упакованного PST-хранилища необходимо реализовать функции, чтобы MAPI и Диспетчер очереди MAPI могли входить в систему поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f92ee-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="f92ee-107">Дополнительные сведения об инициализации и входе в систему поставщика упакованного PST-хранилища можно найти в статье инициализация поставщика упакованного [PST-](initializing-a-wrapped-pst-store-provider.md) хранилища и вход в систему [поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f92ee-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="f92ee-108">Интерфейс **[имаписуппорт:: IUnknown](imapisupportiunknown.md)** предоставляет реализации для задач, которые обычно выполняются поставщиками хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f92ee-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="f92ee-109">Чтобы работать с примером поставщика упакованного PST-хранилища, необходимо обернуть этот интерфейс в оболочку.</span><span class="sxs-lookup"><span data-stu-id="f92ee-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="f92ee-110">Для функции **[имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md)** требуется специальная реализация.</span><span class="sxs-lookup"><span data-stu-id="f92ee-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="f92ee-111">Все остальные функции могут передавать свои параметры базовому объекту, упакованному в оболочку.</span><span class="sxs-lookup"><span data-stu-id="f92ee-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="f92ee-112">В этой статье функция **имаписуппорт:: опенпрофилесектион** демонстрируется с помощью примера кода из примера поставщика УПАКОВАНного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="f92ee-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="f92ee-113">В примере реализуется упакованный поставщик PST, предназначенный для использования вместе с API репликации.</span><span class="sxs-lookup"><span data-stu-id="f92ee-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="f92ee-114">Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-хранилища можно найти в статье [Установка примера поставщика упакованНОГО PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f92ee-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="f92ee-115">Более подробную информацию об API репликации можно узнать [в статье о API репликации](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="f92ee-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="f92ee-116">По завершении работы с поставщиком упакованного PST-хранилища необходимо надлежащим образом завершить работу поставщика упакованного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="f92ee-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="f92ee-117">Дополнительные сведения см. [в разделе Завершение работы поставщика упакованНОГО PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f92ee-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="f92ee-118">Процедура открытия раздела профиля</span><span class="sxs-lookup"><span data-stu-id="f92ee-118">Open Profile Section routine</span></span>

<span data-ttu-id="f92ee-119">Функция **[имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md)** открывает раздел текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="f92ee-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="f92ee-120">Для функции требуется специальная обработка в реализации поставщика упакованного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="f92ee-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="f92ee-121">`pgNSTGlobalProfileSectionGuid` Когда запрашивается запрос, функция возвращает раздел профиля, который кэшируется.</span><span class="sxs-lookup"><span data-stu-id="f92ee-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="f92ee-122">Ксуппорт:: Опенпрофилесектион () пример</span><span class="sxs-lookup"><span data-stu-id="f92ee-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f92ee-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f92ee-123">See also</span></span>

- [<span data-ttu-id="f92ee-124">О примере поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="f92ee-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f92ee-125">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="f92ee-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f92ee-126">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="f92ee-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f92ee-127">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="f92ee-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f92ee-128">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="f92ee-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

