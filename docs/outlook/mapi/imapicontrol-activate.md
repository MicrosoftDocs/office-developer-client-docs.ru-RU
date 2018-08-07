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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: fb6cd23acdb81af250e7e6dfe6facf7226850363
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808823"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="7e9ed-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="7e9ed-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="7e9ed-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e9ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e9ed-105">Выполняет задачи, как отображение диалогового окна или запуск программный операции при нажатии элемента управления кнопка пользователе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="7e9ed-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="7e9ed-106">���������</span><span class="sxs-lookup"><span data-stu-id="7e9ed-106">Parameters</span></span>

 <span data-ttu-id="7e9ed-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e9ed-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7e9ed-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="7e9ed-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7e9ed-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7e9ed-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="7e9ed-110">[in] Дескриптор родительского окна диалоговое окно, на котором отображается элемент управления button.</span><span class="sxs-lookup"><span data-stu-id="7e9ed-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e9ed-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="7e9ed-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7e9ed-112">S_OK</span></span> 
  
> <span data-ttu-id="7e9ed-113">Элемент управления button успешно активирована.</span><span class="sxs-lookup"><span data-stu-id="7e9ed-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e9ed-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e9ed-114">Remarks</span></span>

<span data-ttu-id="7e9ed-115">Метод **IMAPIControl::Activate** выполняет задачи, после щелчка элемента управления button.</span><span class="sxs-lookup"><span data-stu-id="7e9ed-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="7e9ed-116">После завершения нажмите кнопку как часть обработки в таблице отображения MAPI выполняется вызов **активировать** после первого вызова [IMAPIControl::GetState](imapicontrol-getstate.md) для определения, включено ли кнопки.</span><span class="sxs-lookup"><span data-stu-id="7e9ed-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="7e9ed-117">Дополнительные сведения о реализации **активировать** , а другой [IMAPIControl: IUnknown](imapicontroliunknown.md) методы, видеть [Реализации объекта элемента управления](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="7e9ed-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e9ed-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7e9ed-118">See also</span></span>



[<span data-ttu-id="7e9ed-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="7e9ed-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="7e9ed-120">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e9ed-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

