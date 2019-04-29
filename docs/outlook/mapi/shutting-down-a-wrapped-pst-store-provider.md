---
title: Завершение работы поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409946"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="aa289-103">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="aa289-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="aa289-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa289-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa289-105">После завершения работы с упакованным поставщиком хранилища PST-файлов в оболочке необходимо надлежащим образом отключить поставщика упакованного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa289-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="aa289-106">Более подробную информацию об использовании поставщика упакованного PST-хранилища можно узнать в статье [Использование поставщика упакованНОГО PST-хранилища](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aa289-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="aa289-107">Для завершения работы поставщика упакованного PST-хранилища необходимо вызвать функцию **[функцииimsprovider:: Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="aa289-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="aa289-108">Эта функция закрывает поставщика упакованного PST-хранилища в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="aa289-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="aa289-109">В этой статье функция **функцииimsprovider:: Shutdown** показана с помощью примера кода из примера поставщика УПАКОВАНного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa289-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="aa289-110">В примере реализуется упакованный поставщик PST, предназначенный для использования вместе с API репликации.</span><span class="sxs-lookup"><span data-stu-id="aa289-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="aa289-111">Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-хранилища можно найти в статье [Установка примера поставщика упакованНОГО PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aa289-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="aa289-112">Более подробную информацию об API репликации можно узнать [в статье о API репликации](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="aa289-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="aa289-113">Подпрограмма завершения работы</span><span class="sxs-lookup"><span data-stu-id="aa289-113">Shut Down Routine</span></span>

<span data-ttu-id="aa289-114">Диспетчер очереди MAPI вызывает функцию **[функцииimsprovider:: Shutdown](imsprovider-shutdown.md)** непосредственно перед освобождением поставщика УПАКОВАНного PST-хранилища, чтобы поставщик УПАКОВАНного PST-хранилища мог завершить работу должным образом.</span><span class="sxs-lookup"><span data-stu-id="aa289-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="aa289-115">Функция завершает все объекты Session, связанные с поставщиком упакованного PST-хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa289-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="aa289-116">Кмспровидер:: ShutDown () пример</span><span class="sxs-lookup"><span data-stu-id="aa289-116">CMSProvider::ShutDown() Example</span></span>

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a><span data-ttu-id="aa289-117">См. также</span><span class="sxs-lookup"><span data-stu-id="aa289-117">See also</span></span>



[<span data-ttu-id="aa289-118">О примере поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="aa289-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="aa289-119">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="aa289-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="aa289-120">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="aa289-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="aa289-121">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="aa289-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="aa289-122">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="aa289-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

