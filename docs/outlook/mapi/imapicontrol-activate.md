---
title: Имапиконтролактивате
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280204"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="fa623-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="fa623-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="fa623-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa623-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa623-105">Выполняет задачу, например отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения щелкает элемент управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="fa623-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="fa623-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa623-106">Parameters</span></span>

 <span data-ttu-id="fa623-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa623-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fa623-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="fa623-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fa623-109">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="fa623-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="fa623-110">возврата Дескриптор родительского окна диалогового окна, в котором отображается элемент управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="fa623-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa623-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa623-111">Return value</span></span>

<span data-ttu-id="fa623-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa623-112">S_OK</span></span> 
  
> <span data-ttu-id="fa623-113">Элемент управления "Кнопка" успешно активирован.</span><span class="sxs-lookup"><span data-stu-id="fa623-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa623-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fa623-114">Remarks</span></span>

<span data-ttu-id="fa623-115">Метод **имапиконтрол:: Activate** выполняет задачи после нажатия пользователем кнопки элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="fa623-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="fa623-116">После выполнения щелчка в рамках обработки отображаемой таблицы MAPI вызывает **активацию** после первого вызова [имапиконтрол::-State](imapicontrol-getstate.md) , чтобы определить, включена ли кнопка.</span><span class="sxs-lookup"><span data-stu-id="fa623-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="fa623-117">Дополнительные сведения о том, как реализовать **активацию** и другие методы [имапиконтрол: IUnknown](imapicontroliunknown.md) , можно найти в разделе [Реализация объекта Control](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fa623-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa623-118">См. также</span><span class="sxs-lookup"><span data-stu-id="fa623-118">See also</span></span>



[<span data-ttu-id="fa623-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="fa623-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="fa623-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa623-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

