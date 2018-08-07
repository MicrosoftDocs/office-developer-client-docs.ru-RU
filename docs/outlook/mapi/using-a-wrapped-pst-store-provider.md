---
title: С помощью оболочку поставщика хранилища PST-файлов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812571"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="9c3c6-103">С помощью оболочку поставщика хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="9c3c6-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="9c3c6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c3c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c3c6-105">Прежде чем использовать оболочку поставщика хранилища личных папок (PST) файла, необходимо инициализировать и настроить оболочку поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="9c3c6-106">После настройки оболочку поставщика хранилища PST-файлов, необходимо реализовать функции, чтобы MAPI и диспетчер очереди MAPI могут войти на поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="9c3c6-107">Дополнительные сведения об инициализации и вход в систему на оболочку поставщик хранилища PST-файлов можно [инициализации поставщика оболочку хранения PST -файлов](initializing-a-wrapped-pst-store-provider.md) и [Ведение журнала на к поставщику хранения оболочку PST -файлов](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9c3c6-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="9c3c6-108">Интерфейс **[IMAPISupport::IUnknown](imapisupportiunknown.md)** включает сведения о реализации для задач, которые обычно выполняются с сообщение хранения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="9c3c6-109">Этот интерфейс должен оболочку для оболочку PST поставщик хранилища для работы.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="9c3c6-110">Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** требует специальных реализаций.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="9c3c6-111">Другие функции можно передать свои параметры базового объекта оболочку.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="9c3c6-112">В этом разделе демонстрируется функция **IMAPISupport::OpenProfileSection** с помощью пример кода из оболочку PST поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="9c3c6-113">В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="9c3c6-114">Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="9c3c6-115">Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="9c3c6-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="9c3c6-116">После завершения работы с оболочкой поставщика хранилища PST-файлов, необходимо правильно выключить оболочку поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="9c3c6-117">Для получения дополнительных сведений см [Завершает работу оболочку PST поставщика хранилища](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9c3c6-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="9c3c6-118">Открытие раздела профиля общей процедуры</span><span class="sxs-lookup"><span data-stu-id="9c3c6-118">Open Profile Section routine</span></span>

<span data-ttu-id="9c3c6-119">Функция **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** откроется раздел текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="9c3c6-120">Функции требуется особая обработка выполняется в оболочку реализации поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="9c3c6-121">При `pgNSTGlobalProfileSectionGuid` запрашивается, функция возвращает раздела профиля кэширования.</span><span class="sxs-lookup"><span data-stu-id="9c3c6-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="9c3c6-122">Пример CSupport::OpenProfileSection()</span><span class="sxs-lookup"><span data-stu-id="9c3c6-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9c3c6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9c3c6-123">See also</span></span>

- [<span data-ttu-id="9c3c6-124">Сведения о примере поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="9c3c6-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="9c3c6-125">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="9c3c6-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="9c3c6-126">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="9c3c6-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="9c3c6-127">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="9c3c6-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="9c3c6-128">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="9c3c6-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

