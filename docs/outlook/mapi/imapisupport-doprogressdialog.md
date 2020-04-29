---
title: имаписуппортдопрогрессдиалог
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
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="c26ba-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="c26ba-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="c26ba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c26ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c26ba-105">Получает объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c26ba-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="c26ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c26ba-106">Parameters</span></span>

 <span data-ttu-id="c26ba-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="c26ba-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c26ba-108">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c26ba-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="c26ba-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c26ba-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c26ba-110">возврата Битовая маска флагов, определяющих способ вычисления объекта хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c26ba-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="c26ba-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c26ba-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c26ba-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="c26ba-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="c26ba-113">Ход выполнения вычисляется для элемента верхнего уровня, например для родительской папки.</span><span class="sxs-lookup"><span data-stu-id="c26ba-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="c26ba-114">Объект Progress должен использовать значения в параметрах _улкаунт_ и _ултотал_ метода [IMAPIProgress::P рогресс](imapiprogress-progress.md) , которые указывают текущий элемент и общее количество элементов в операции, соответственно, для увеличения индикатора хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c26ba-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="c26ba-115">_лпппрогресс_</span><span class="sxs-lookup"><span data-stu-id="c26ba-115">_lppProgress_</span></span>
  
> <span data-ttu-id="c26ba-116">вышли Указатель на указатель на объект хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c26ba-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c26ba-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c26ba-117">Return value</span></span>

<span data-ttu-id="c26ba-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c26ba-118">S_OK</span></span> 
  
> <span data-ttu-id="c26ba-119">Объект Progress успешно получен.</span><span class="sxs-lookup"><span data-stu-id="c26ba-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c26ba-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c26ba-120">Remarks</span></span>

<span data-ttu-id="c26ba-121">Метод **имаписуппорт::D опрогрессдиалог** реализован для адресных книг и объектов поддержки поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c26ba-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="c26ba-122">Эти поставщики вызывают **допрогрессдиалог** для доступа к реализации MAPI интерфейса [IMAPIProgress](imapiprogressiunknown.md) , который вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c26ba-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="c26ba-123">Сведения о том, как использовать объект Progress и интерфейс **IMAPIProgress** , приведены в разделе [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="c26ba-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c26ba-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c26ba-124">See also</span></span>



[<span data-ttu-id="c26ba-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c26ba-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="c26ba-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="c26ba-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="c26ba-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c26ba-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="c26ba-128">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="c26ba-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

