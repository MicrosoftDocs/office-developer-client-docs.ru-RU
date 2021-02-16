---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409911"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="d0415-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="d0415-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="d0415-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0415-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0415-105">Предоставляет управление ЦП для пула MAPI, чтобы он выполнял любые задачи, которые он считает необходимыми.</span><span class="sxs-lookup"><span data-stu-id="d0415-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d0415-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0415-106">Parameters</span></span>

 <span data-ttu-id="d0415-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0415-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d0415-108">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="d0415-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0415-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0415-109">Return value</span></span>

<span data-ttu-id="d0415-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0415-110">S_OK</span></span> 
  
> <span data-ttu-id="d0415-111">Поставщик транспорта успешно выпустил ЦП.</span><span class="sxs-lookup"><span data-stu-id="d0415-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="d0415-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d0415-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="d0415-113">Предписывает поставщику транспорта остановить доставку сообщения получателям, которые еще не получили его.</span><span class="sxs-lookup"><span data-stu-id="d0415-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0415-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0415-114">Remarks</span></span>

<span data-ttu-id="d0415-115">Метод **IMAPISupport::SpoolerYield** реализован для объектов поддержки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d0415-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="d0415-116">Поставщики транспорта **звонят SpoolerYield,** чтобы позволить пулу MAPI выполнять любую необходимую обработку.</span><span class="sxs-lookup"><span data-stu-id="d0415-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d0415-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d0415-117">Notes to callers</span></span>

<span data-ttu-id="d0415-118">Вызовите **SpoolerYield** при выполнении длительных операций, которые можно приостановить.</span><span class="sxs-lookup"><span data-stu-id="d0415-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="d0415-119">Это позволяет запускать приложения переднего плана во время длительной операции, например доставки в большой список получателей по сети занятости.</span><span class="sxs-lookup"><span data-stu-id="d0415-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="d0415-120">Если **SpoolerYield** возвращается с MAPI_W_CANCEL_MESSAGE, то пульщик MAPI определил, что сообщение больше не следует отправлять.</span><span class="sxs-lookup"><span data-stu-id="d0415-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="d0415-121">Вернетесь MAPI_E_USER_CANCEL к вызываемой процедуре и по возможности выйдите из нее.</span><span class="sxs-lookup"><span data-stu-id="d0415-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="d0415-122">Дополнительные сведения о выходе из пула MAPI см. в этой [теме.](interacting-with-the-mapi-spooler.md)</span><span class="sxs-lookup"><span data-stu-id="d0415-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0415-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d0415-123">See also</span></span>



[<span data-ttu-id="d0415-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0415-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

