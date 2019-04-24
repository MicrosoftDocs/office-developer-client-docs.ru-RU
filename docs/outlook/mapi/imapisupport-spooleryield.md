---
title: Имаписуппортспулериелд
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329040"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="ead0b-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="ead0b-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="ead0b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ead0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ead0b-105">Предоставляет управление ЦП диспетчеру очереди MAPI, чтобы он мог выполнять любые задачи, которые он считает необходимым.</span><span class="sxs-lookup"><span data-stu-id="ead0b-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ead0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ead0b-106">Parameters</span></span>

 <span data-ttu-id="ead0b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ead0b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ead0b-108">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ead0b-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ead0b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ead0b-109">Return value</span></span>

<span data-ttu-id="ead0b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ead0b-110">S_OK</span></span> 
  
> <span data-ttu-id="ead0b-111">Поставщик транспорта успешно освободил ЦП.</span><span class="sxs-lookup"><span data-stu-id="ead0b-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="ead0b-112">МАПИ_В_КАНЦЕЛ_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="ead0b-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="ead0b-113">ПредПисывает поставщику транспорта прекратить доставку сообщения всем получателям, которые еще не получили его.</span><span class="sxs-lookup"><span data-stu-id="ead0b-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ead0b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ead0b-114">Remarks</span></span>

<span data-ttu-id="ead0b-115">Метод **имаписуппорт:: спулериелд** реализован для объектов поддержки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ead0b-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="ead0b-116">Поставщики транспорта вызывают **спулериелд** , чтобы разрешить диспетчеру очереди MAPI выполнить необходимую обработку.</span><span class="sxs-lookup"><span data-stu-id="ead0b-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ead0b-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ead0b-117">Notes to callers</span></span>

<span data-ttu-id="ead0b-118">ВыЗывайте **спулериелд** при выполнении длительных операций, которые можно приостановить.</span><span class="sxs-lookup"><span data-stu-id="ead0b-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="ead0b-119">Это позволяет приложениям переднего плана выполняться во время длительной операции, например при доставке большого списка получателей в занятой сети.</span><span class="sxs-lookup"><span data-stu-id="ead0b-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="ead0b-120">Если **спулериелд** ВОЗВРАЩАЕТ с мапи_в_канцел_мессаже, то диспетчер очереди MAPI обнаружил, что сообщение больше не должно отправляться.</span><span class="sxs-lookup"><span data-stu-id="ead0b-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="ead0b-121">ВозВращайте МАПИ_Е_УСЕР_КАНЦЕЛ к вызывающему процессу и выйдите из него, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ead0b-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="ead0b-122">Для получения дополнительных сведений о возможностях диспетчера очереди MAPI обратитесь к разделу [взаимодействие с диспетчерОм очереди MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="ead0b-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ead0b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ead0b-123">See also</span></span>



[<span data-ttu-id="ead0b-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ead0b-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

