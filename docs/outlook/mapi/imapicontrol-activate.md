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
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580686"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="1002d-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="1002d-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="1002d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1002d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1002d-105">Выполняет задачи, как отображение диалогового окна или запуск программный операции при нажатии элемента управления кнопка пользователе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="1002d-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="1002d-106">���������</span><span class="sxs-lookup"><span data-stu-id="1002d-106">Parameters</span></span>

 <span data-ttu-id="1002d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1002d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1002d-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="1002d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1002d-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1002d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="1002d-110">[in] Дескриптор родительского окна диалоговое окно, на котором отображается элемент управления button.</span><span class="sxs-lookup"><span data-stu-id="1002d-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1002d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1002d-111">Return value</span></span>

<span data-ttu-id="1002d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1002d-112">S_OK</span></span> 
  
> <span data-ttu-id="1002d-113">Элемент управления button успешно активирована.</span><span class="sxs-lookup"><span data-stu-id="1002d-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1002d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1002d-114">Remarks</span></span>

<span data-ttu-id="1002d-115">Метод **IMAPIControl::Activate** выполняет задачи, после щелчка элемента управления button.</span><span class="sxs-lookup"><span data-stu-id="1002d-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="1002d-116">После завершения нажмите кнопку как часть обработки в таблице отображения MAPI выполняется вызов **активировать** после первого вызова [IMAPIControl::GetState](imapicontrol-getstate.md) для определения, включено ли кнопки.</span><span class="sxs-lookup"><span data-stu-id="1002d-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="1002d-117">Дополнительные сведения о реализации **активировать** , а другой [IMAPIControl: IUnknown](imapicontroliunknown.md) методы, видеть [Реализации объекта элемента управления](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1002d-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1002d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="1002d-118">See also</span></span>



[<span data-ttu-id="1002d-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="1002d-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="1002d-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1002d-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

