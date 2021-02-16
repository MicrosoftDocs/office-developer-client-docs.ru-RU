---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418017"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="3837a-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="3837a-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="3837a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3837a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3837a-105">Выполняет такую задачу, как отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения нажимает кнопку управления.</span><span class="sxs-lookup"><span data-stu-id="3837a-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="3837a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3837a-106">Parameters</span></span>

 <span data-ttu-id="3837a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3837a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3837a-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="3837a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3837a-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3837a-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="3837a-110">[in] Handle to the parent window of the dialog box on which the button control appears.</span><span class="sxs-lookup"><span data-stu-id="3837a-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3837a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3837a-111">Return value</span></span>

<span data-ttu-id="3837a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3837a-112">S_OK</span></span> 
  
> <span data-ttu-id="3837a-113">Кнопка управления успешно активирована.</span><span class="sxs-lookup"><span data-stu-id="3837a-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3837a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3837a-114">Remarks</span></span>

<span data-ttu-id="3837a-115">Метод **IMAPIControl::Activate** выполняет задачи после нажатия пользователем кнопки.</span><span class="sxs-lookup"><span data-stu-id="3837a-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="3837a-116">После нажатия в рамках обработки таблицы отображения MAPI вызывает  активацию после первого вызова [IMAPIControl::GetState,](imapicontrol-getstate.md) чтобы определить, включена ли кнопка.</span><span class="sxs-lookup"><span data-stu-id="3837a-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="3837a-117">Дополнительные сведения о реализации **метода Activate** и других методов [IMAPIControl : IUnknown](imapicontroliunknown.md) см. в реализации [объекта control.](control-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="3837a-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3837a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3837a-118">See also</span></span>



[<span data-ttu-id="3837a-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="3837a-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="3837a-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3837a-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

