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
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809129"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="440f3-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="440f3-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="440f3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="440f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="440f3-105">Извлекает объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="440f3-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="440f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="440f3-106">Parameters</span></span>

 <span data-ttu-id="440f3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="440f3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="440f3-108">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="440f3-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="440f3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="440f3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="440f3-110">[in] Битовая маска флаги, который управляет расчет хода выполнения, в объекте хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="440f3-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="440f3-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="440f3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="440f3-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="440f3-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="440f3-113">Ход выполнения рассчитывается для элемент верхнего уровня, например родительской папки.</span><span class="sxs-lookup"><span data-stu-id="440f3-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="440f3-114">Объект хода выполнения следует использовать значения в параметры метода [IMAPIProgress::Progress](imapiprogress-progress.md) _инициализирует метод ulCount_ и _ulTotal_ — указывающие текущего элемента и итоговых значений в операции, соответственно — для увеличения хода выполнения обновления индикатор для операции.</span><span class="sxs-lookup"><span data-stu-id="440f3-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="440f3-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="440f3-115">_lppProgress_</span></span>
  
> <span data-ttu-id="440f3-116">[out] Указатель на указатель на объект хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="440f3-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="440f3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="440f3-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="440f3-118">S_OK</span></span> 
  
> <span data-ttu-id="440f3-119">Ход выполнения объект был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="440f3-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="440f3-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="440f3-120">Remarks</span></span>

<span data-ttu-id="440f3-121">Метод **IMAPISupport::DoProgressDialog** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки.</span><span class="sxs-lookup"><span data-stu-id="440f3-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="440f3-122">Эти поставщики вызов **DoProgressDialog** для доступа к MAPI реализации интерфейса [IMAPIProgress](imapiprogressiunknown.md) , которая вычисляет сведения о ходе выполнения и отображает стандартное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="440f3-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="440f3-123">Для получения сведений об использовании объекта хода выполнения и интерфейс **IMAPIProgress** просмотрите [представление индикатор хода выполнения](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="440f3-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="440f3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="440f3-124">See also</span></span>



[<span data-ttu-id="440f3-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="440f3-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="440f3-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="440f3-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="440f3-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="440f3-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="440f3-128">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="440f3-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

