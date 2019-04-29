---
title: Имапивиевадвисесинконпринт
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406173"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="19ee6-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="19ee6-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="19ee6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19ee6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19ee6-105">Уведомляет средство просмотра форм о состоянии печати формы.</span><span class="sxs-lookup"><span data-stu-id="19ee6-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="19ee6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19ee6-106">Parameters</span></span>

 <span data-ttu-id="19ee6-107">_Двпаженумбер_</span><span class="sxs-lookup"><span data-stu-id="19ee6-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="19ee6-108">возврата Номер последней напечатанной страницы.</span><span class="sxs-lookup"><span data-stu-id="19ee6-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="19ee6-109">_Хрстатус_</span><span class="sxs-lookup"><span data-stu-id="19ee6-109">_hrStatus_</span></span>
  
> <span data-ttu-id="19ee6-110">возврата Значение HRESULT, указывающее состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="19ee6-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="19ee6-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="19ee6-111">Possible values are:</span></span>
    
<span data-ttu-id="19ee6-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="19ee6-112">S_FALSE</span></span> 
  
> <span data-ttu-id="19ee6-113">Задание печати успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="19ee6-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="19ee6-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="19ee6-114">S_OK</span></span> 
  
> <span data-ttu-id="19ee6-115">Выполняется задание печати.</span><span class="sxs-lookup"><span data-stu-id="19ee6-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="19ee6-116">СБОЕВ</span><span class="sxs-lookup"><span data-stu-id="19ee6-116">FAILED</span></span> 
  
> <span data-ttu-id="19ee6-117">Задание печати прервано из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="19ee6-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19ee6-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19ee6-118">Return value</span></span>

<span data-ttu-id="19ee6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="19ee6-119">S_OK</span></span> 
  
> <span data-ttu-id="19ee6-120">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="19ee6-120">The notification succeeded.</span></span>
    
<span data-ttu-id="19ee6-121">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="19ee6-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="19ee6-122">Пользователь отменил операцию, как правило, нажав кнопку Отмена в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="19ee6-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="19ee6-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="19ee6-123">Remarks</span></span>

<span data-ttu-id="19ee6-124">Объекты форм вызывают метод **имапивиевадвисесинк:: OnPrint** при печати для информирования средства просмотра о ходе печати.</span><span class="sxs-lookup"><span data-stu-id="19ee6-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="19ee6-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="19ee6-125">Notes to callers</span></span>

<span data-ttu-id="19ee6-126">Если задание печати включает несколько страниц, вы можете вызвать функцию **OnPrint** после печати каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="19ee6-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="19ee6-127">Задайте для _двпаженумбер_ страницу, которая печатается в данный момент, и _ХРСТАТУС_ в значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="19ee6-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="19ee6-128">После завершения задания печати вызовите функцию **OnPrint** с _двпаженумбер_ , установленной на последнюю страницу, и _хрстатус_ значение S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="19ee6-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="19ee6-129">Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="19ee6-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19ee6-130">См. также</span><span class="sxs-lookup"><span data-stu-id="19ee6-130">See also</span></span>



[<span data-ttu-id="19ee6-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19ee6-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

