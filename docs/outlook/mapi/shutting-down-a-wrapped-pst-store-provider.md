---
title: Завершение работы поставщика упакованного PST-магазина
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409946"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="41f30-103">Завершение работы поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="41f30-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="41f30-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41f30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41f30-105">После завершения работы с поставщиком упакованного PST-файла необходимо завершить работу поставщика упакованного PST-магазина.</span><span class="sxs-lookup"><span data-stu-id="41f30-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="41f30-106">Дополнительные сведения об использовании поставщика упакованного PST-магазина см. в сведениях об использовании поставщика упакованного [PST-магазина.](using-a-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="41f30-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="41f30-107">Чтобы отключить поставщика упакованного PST-магазина, необходимо вызвать функцию **[IMSProvider::Shutdown.](imsprovider-shutdown.md)**</span><span class="sxs-lookup"><span data-stu-id="41f30-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="41f30-108">Эта функция закрывает поставщика упакованного PST-магазина в упорядоченном порядке.</span><span class="sxs-lookup"><span data-stu-id="41f30-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="41f30-109">В этом разделе функция **IMSProvider::Shutdown** демонстрируется с помощью примера кода из примера поставщика упакованного PST-магазина.</span><span class="sxs-lookup"><span data-stu-id="41f30-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="41f30-110">В примере реализован упакованный поставщик PST,который предназначен для использования в сочетании с API репликации.</span><span class="sxs-lookup"><span data-stu-id="41f30-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="41f30-111">Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-магазина см. в установке примера поставщика упакованного [PST-магазина.](installing-the-sample-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="41f30-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="41f30-112">Дополнительные сведения об API репликации см. в сведениях [об API репликации.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="41f30-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="41f30-113">Завершение работы программы</span><span class="sxs-lookup"><span data-stu-id="41f30-113">Shut Down Routine</span></span>

<span data-ttu-id="41f30-114">Пулер MAPI вызывает функцию **[IMSProvider::Shutdown](imsprovider-shutdown.md)** непосредственно перед выпуском поставщика упакованного PST-магазина, чтобы поставщик упакованного PST-магазина можно было должным образом отключить.</span><span class="sxs-lookup"><span data-stu-id="41f30-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="41f30-115">Эта функция завершает все объекты сеанса, связанные с поставщиком упакованного PST-хранения.</span><span class="sxs-lookup"><span data-stu-id="41f30-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="41f30-116">Пример CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="41f30-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="41f30-117">См. также</span><span class="sxs-lookup"><span data-stu-id="41f30-117">See also</span></span>



[<span data-ttu-id="41f30-118">Пример поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="41f30-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="41f30-119">Установка примера поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="41f30-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="41f30-120">Инициализация поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="41f30-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="41f30-121">Вход в систему поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="41f30-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="41f30-122">Использование поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="41f30-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

