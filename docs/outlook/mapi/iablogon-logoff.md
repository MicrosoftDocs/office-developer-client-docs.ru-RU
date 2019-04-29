---
title: Иаблогонлогофф
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416400"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="50d88-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="50d88-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="50d88-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50d88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50d88-105">Инициирует процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="50d88-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="50d88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50d88-106">Parameters</span></span>

 <span data-ttu-id="50d88-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50d88-107">_ulFlags_</span></span>
  
> <span data-ttu-id="50d88-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="50d88-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50d88-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50d88-109">Return value</span></span>

<span data-ttu-id="50d88-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="50d88-110">S_OK</span></span> 
  
> <span data-ttu-id="50d88-111">Процесс выхода был успешно запущен.</span><span class="sxs-lookup"><span data-stu-id="50d88-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50d88-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="50d88-112">Remarks</span></span>

<span data-ttu-id="50d88-113">Процесс выхода из системы обычно запускается, когда клиент вызывает метод [IMAPISession:: logoff](imapisession-logoff.md) для завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="50d88-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="50d88-114">Затем MAPI вызывает метод **иаблогон:: logoff** поставщика адресных книг для запуска процесса выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="50d88-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="50d88-115">Метод **иаблогон:: logoff** выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="50d88-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="50d88-116">Освобождает все открытые объекты, например любые подобъекты или объект Status.</span><span class="sxs-lookup"><span data-stu-id="50d88-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="50d88-117">Освобождает объект поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="50d88-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="50d88-118">Дополнительные сведения о процессе выхода из системы поставщиков адресных книг приведены в разделе [Завершение работы поставщика услуг](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="50d88-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50d88-119">См. также</span><span class="sxs-lookup"><span data-stu-id="50d88-119">See also</span></span>



[<span data-ttu-id="50d88-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="50d88-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="50d88-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50d88-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

