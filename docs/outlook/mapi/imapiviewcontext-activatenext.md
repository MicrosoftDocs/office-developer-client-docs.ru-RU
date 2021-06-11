---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410618"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="30ebc-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="30ebc-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="30ebc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ebc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ebc-105">Активирует следующее или предыдущее сообщение в порядке представления.</span><span class="sxs-lookup"><span data-stu-id="30ebc-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="30ebc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="30ebc-106">Parameters</span></span>

<span data-ttu-id="30ebc-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="30ebc-107">_ulDir_</span></span>
  
> <span data-ttu-id="30ebc-108">[in] Флаги состояния, которые дают сведения об активированном сообщении.</span><span class="sxs-lookup"><span data-stu-id="30ebc-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="30ebc-109">Допустимые параметры флага:</span><span class="sxs-lookup"><span data-stu-id="30ebc-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="30ebc-110">VCDIR_CATEGORY. Просмотр должен активировать сообщение в другой категории представления.</span><span class="sxs-lookup"><span data-stu-id="30ebc-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="30ebc-111">Необходимо активировать сообщение:</span><span class="sxs-lookup"><span data-stu-id="30ebc-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="30ebc-112">Первое сообщение в следующей категории представлений, если этот флаг **или** ed с VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="30ebc-112">The first message in the next view category if this flag is **OR** ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="30ebc-113">Последнее сообщение в предыдущей категории представлений, если этот флаг или VCDIR_PREV, а предыдущая категория расширена. </span><span class="sxs-lookup"><span data-stu-id="30ebc-113">The last message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="30ebc-114">Первое сообщение в предыдущей категории представлений, если этот флаг или VCDIR_PREV и предыдущая категория не расширена. </span><span class="sxs-lookup"><span data-stu-id="30ebc-114">The first message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="30ebc-115">В этом случае предыдущая категория проходит автоматическое расширение.</span><span class="sxs-lookup"><span data-stu-id="30ebc-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="30ebc-116">VCDIR_DELETE. Просмотр должен активировать следующее или предыдущее сообщение, так как текущее сообщение удалено.</span><span class="sxs-lookup"><span data-stu-id="30ebc-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="30ebc-117">VCDIR_MOVE. Просмотр должен активировать следующее или предыдущее сообщение, так как текущее сообщение было перемещено.</span><span class="sxs-lookup"><span data-stu-id="30ebc-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="30ebc-118">VCDIR_NEXT. Просмотр должен активировать следующее сообщение в порядке представления.</span><span class="sxs-lookup"><span data-stu-id="30ebc-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="30ebc-119">VCDIR_PREV. Просмотр должен активировать предыдущее сообщение в порядке представления.</span><span class="sxs-lookup"><span data-stu-id="30ebc-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="30ebc-120">VCDIR_UNREAD. В порядке представления зрителю следует активировать следующее или предыдущее непрочитанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="30ebc-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="30ebc-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="30ebc-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="30ebc-122">[in] Указатель на структуру Windows **reCT,** содержащую размер и положение окна, которое будет использоваться для отображения активированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="30ebc-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="30ebc-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30ebc-123">Return value</span></span>

<span data-ttu-id="30ebc-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="30ebc-124">S_OK</span></span> 
  
> <span data-ttu-id="30ebc-125">Сообщение было активировано успешно.</span><span class="sxs-lookup"><span data-stu-id="30ebc-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="30ebc-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="30ebc-126">S_FALSE</span></span> 
  
> <span data-ttu-id="30ebc-127">Сообщение было активировано успешно, но в процессе был открыт другой тип формы.</span><span class="sxs-lookup"><span data-stu-id="30ebc-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30ebc-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="30ebc-128">Remarks</span></span>

<span data-ttu-id="30ebc-129">Объекты формы звонят **методу IMAPIViewContext::ActivateNext,** чтобы изменить отображаемую пользователю сообщение.</span><span class="sxs-lookup"><span data-stu-id="30ebc-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="30ebc-130">Значение, переданное в  _параметре ulDir,_ указывает, какое сообщение следует активировать и, в некоторых случаях, почему.</span><span class="sxs-lookup"><span data-stu-id="30ebc-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="30ebc-131">Флаги VCDIR_NEXT и VCDIR_PREVIOUS соответствуют пользователям, выбрав в представлении команду **Next** или **Previous** соответственно.</span><span class="sxs-lookup"><span data-stu-id="30ebc-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="30ebc-132">Эти операции обычно соответствуют перемещению вверх или вниз одного сообщения в списке сообщений для просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="30ebc-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="30ebc-133">Флаги VCDIR_DELETE и VCDIR_MOVE установлены методами [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) и [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="30ebc-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="30ebc-134">Реализация этих методов вызвать **ActivateNext** с соответствующим направлением, а затем выполнить запрашиваемую операцию на сообщении, если **вызов ActivateNext** не сбой.</span><span class="sxs-lookup"><span data-stu-id="30ebc-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="30ebc-135">Как правило, зрители форм позволяют пользователям указывать направление перемещения в списке сообщений.</span><span class="sxs-lookup"><span data-stu-id="30ebc-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="30ebc-136">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="30ebc-136">Notes to implementers</span></span>

<span data-ttu-id="30ebc-137">Реализация [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) делает следующее или предыдущее сообщение в папке в зависимости от значения  _ulDir_, текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="30ebc-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="30ebc-138">После **возвращения ActivatNext** позвоните [в IMAPIMessageSite::GetMessage,](imapimessagesite-getmessage.md) чтобы получить указатель на вновь активированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="30ebc-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="30ebc-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="30ebc-139">Notes to callers</span></span>

<span data-ttu-id="30ebc-140">Если **activateNext** возвращает S_FALSE или если текущего сообщения нет, выполните обычную процедуру остановки, которая должна включать вызов метода [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) вашей формы.</span><span class="sxs-lookup"><span data-stu-id="30ebc-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="30ebc-141">Если отображается следующее или предыдущее сообщение, используйте прямоугольник окна, переданный в  _параметре prcPosRect,_ чтобы отобразить его.</span><span class="sxs-lookup"><span data-stu-id="30ebc-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="30ebc-142">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="30ebc-142">MFCMAPI reference</span></span>

<span data-ttu-id="30ebc-143">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="30ebc-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="30ebc-144">**Файл**</span><span class="sxs-lookup"><span data-stu-id="30ebc-144">**File**</span></span>|<span data-ttu-id="30ebc-145">**Функция**</span><span class="sxs-lookup"><span data-stu-id="30ebc-145">**Function**</span></span>|<span data-ttu-id="30ebc-146">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="30ebc-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30ebc-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="30ebc-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="30ebc-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="30ebc-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="30ebc-149">MFCMAPI реализует метод **IMAPIViewContext::ActivateNext** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="30ebc-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30ebc-150">См. также</span><span class="sxs-lookup"><span data-stu-id="30ebc-150">See also</span></span>

- [<span data-ttu-id="30ebc-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="30ebc-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="30ebc-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30ebc-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="30ebc-153">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="30ebc-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

