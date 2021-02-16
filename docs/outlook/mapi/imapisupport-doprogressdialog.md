---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432585"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="67cac-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="67cac-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="67cac-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67cac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67cac-105">Извлекает объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="67cac-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="67cac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67cac-106">Parameters</span></span>

 <span data-ttu-id="67cac-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="67cac-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="67cac-108">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="67cac-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="67cac-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="67cac-109">_ulFlags_</span></span>
  
> <span data-ttu-id="67cac-110">[in] Битоваяmas флагов, которая управляет тем, как объект хода выполнения должен вычислять ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="67cac-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="67cac-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="67cac-111">The following flag can be set:</span></span>
    
<span data-ttu-id="67cac-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="67cac-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="67cac-113">Ход выполнения рассчитывается для элемента верхнего уровня, например родительской папки.</span><span class="sxs-lookup"><span data-stu-id="67cac-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="67cac-114">Объект progress должен использовать значения в параметрах _ulCount_ и _ulTotal_ метода [IMAPIProgress::P gress,](imapiprogress-progress.md) которые указывают текущий элемент и общее число элементов в операции соответственно, для инкремента индикатора хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="67cac-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="67cac-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="67cac-115">_lppProgress_</span></span>
  
> <span data-ttu-id="67cac-116">[out] Указатель на указатель на объект хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="67cac-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67cac-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67cac-117">Return value</span></span>

<span data-ttu-id="67cac-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="67cac-118">S_OK</span></span> 
  
> <span data-ttu-id="67cac-119">Объект progress был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="67cac-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67cac-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="67cac-120">Remarks</span></span>

<span data-ttu-id="67cac-121">Метод **IMAPISupport::D oProgressDialog** реализован для объектов поддержки поставщиков адресной книги и хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="67cac-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="67cac-122">Эти поставщики **вызывают DoProgressDialog** для доступа к реализации MAPI [интерфейса IMAPIProgress,](imapiprogressiunknown.md) который вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="67cac-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="67cac-123">Сведения об использовании объекта хода выполнения и **интерфейса IMAPIProgress** см. в подразделе ["Отображение индикатора хода выполнения".](how-to-display-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="67cac-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67cac-124">См. также</span><span class="sxs-lookup"><span data-stu-id="67cac-124">See also</span></span>



[<span data-ttu-id="67cac-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67cac-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="67cac-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="67cac-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="67cac-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="67cac-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="67cac-128">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="67cac-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

