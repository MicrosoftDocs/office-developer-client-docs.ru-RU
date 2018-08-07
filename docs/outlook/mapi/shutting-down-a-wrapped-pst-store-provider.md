---
title: Завершение работы поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812287"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="6fc72-103">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="6fc72-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="6fc72-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fc72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fc72-105">После завершения работы с оболочку поставщика хранилища личных папок (PST) файла, необходимо надлежащим образом завершение работы оболочку поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="6fc72-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="6fc72-106">Дополнительные сведения об использовании оболочку поставщика хранилища PST-файлов [с использованием поставщика оболочку хранения PST -файлов](using-a-wrapped-pst-store-provider.md)см.</span><span class="sxs-lookup"><span data-stu-id="6fc72-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="6fc72-107">Завершение работы оболочку поставщика хранилища PST-файлов, необходимо вызвать функцию **[IMSProvider::Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="6fc72-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="6fc72-108">Закрывает этой функции вниз оболочку поставщика хранилища PST определенным образом.</span><span class="sxs-lookup"><span data-stu-id="6fc72-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="6fc72-109">В этом разделе демонстрируется функция **IMSProvider::Shutdown** с помощью пример кода из оболочку PST поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="6fc72-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="6fc72-110">В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации.</span><span class="sxs-lookup"><span data-stu-id="6fc72-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="6fc72-111">Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см.</span><span class="sxs-lookup"><span data-stu-id="6fc72-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="6fc72-112">Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="6fc72-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="6fc72-113">Завершение работы программы</span><span class="sxs-lookup"><span data-stu-id="6fc72-113">Shut Down Routine</span></span>

<span data-ttu-id="6fc72-114">Диспетчер очереди MAPI вызывает функцию **[IMSProvider::Shutdown](imsprovider-shutdown.md)** перед освобождает оболочку поставщика хранилища PST-файлов, чтобы оболочку поставщика хранилища PST-файлов можно завершить работу должным образом.</span><span class="sxs-lookup"><span data-stu-id="6fc72-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="6fc72-115">Функция завершает работу всех объектов сеанса, связанных с переносами поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="6fc72-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="6fc72-116">Пример CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="6fc72-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6fc72-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6fc72-117">See also</span></span>



[<span data-ttu-id="6fc72-118">Сведения о примере поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="6fc72-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6fc72-119">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="6fc72-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6fc72-120">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="6fc72-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6fc72-121">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="6fc72-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="6fc72-122">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="6fc72-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

