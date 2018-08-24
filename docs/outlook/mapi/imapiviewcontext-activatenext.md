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
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588505"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="f83d3-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f83d3-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="f83d3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f83d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f83d3-105">Активирует следующий или предыдущий сообщения в том порядке, представление.</span><span class="sxs-lookup"><span data-stu-id="f83d3-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="f83d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f83d3-106">Parameters</span></span>

<span data-ttu-id="f83d3-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="f83d3-107">_ulDir_</span></span>
  
> <span data-ttu-id="f83d3-108">[in] Предоставление сведений о сообщении активируется флаги состояния.</span><span class="sxs-lookup"><span data-stu-id="f83d3-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="f83d3-109">Допустимый флаг следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f83d3-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="f83d3-110">VCDIR_CATEGORY: Средство просмотра должно быть активировано сообщения в другой категории представления.</span><span class="sxs-lookup"><span data-stu-id="f83d3-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="f83d3-111">— Это сообщение, чтобы активировать:</span><span class="sxs-lookup"><span data-stu-id="f83d3-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="f83d3-112">Первое сообщение в категории, если этот флаг **или**ed с VCDIR_NEXT следующего представления.</span><span class="sxs-lookup"><span data-stu-id="f83d3-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="f83d3-113">Последние сообщения в предыдущей категории представления, если этот флаг ed **или**с VCDIR_PREV и предыдущих категории развернут.</span><span class="sxs-lookup"><span data-stu-id="f83d3-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="f83d3-114">Первое сообщение в предыдущем категории и предыдущей категории представления, если этот флаг ed **или**с VCDIR_PREV еще не развернут.</span><span class="sxs-lookup"><span data-stu-id="f83d3-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="f83d3-115">В этом случае предыдущей категории проходит автоматического развертывания.</span><span class="sxs-lookup"><span data-stu-id="f83d3-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="f83d3-116">VCDIR_DELETE: Средство просмотра должно быть активировано следующий или предыдущий сообщения текущего сообщения были удалены.</span><span class="sxs-lookup"><span data-stu-id="f83d3-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="f83d3-117">VCDIR_MOVE: Средство просмотра должно быть активировано следующий или предыдущий сообщение так, как была перемещена текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f83d3-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="f83d3-118">VCDIR_NEXT: Средство просмотра должно быть активировано следующее сообщение в порядке представления.</span><span class="sxs-lookup"><span data-stu-id="f83d3-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="f83d3-119">VCDIR_PREV: Средство просмотра должно быть активировано предыдущее сообщение в том порядке, представление.</span><span class="sxs-lookup"><span data-stu-id="f83d3-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="f83d3-120">VCDIR_UNREAD: Средство просмотра должно быть активировано следующий или предыдущий непрочитанные сообщения в том порядке, представление.</span><span class="sxs-lookup"><span data-stu-id="f83d3-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="f83d3-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="f83d3-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="f83d3-122">[in] Указатель на Windows **Прямоугольник** структура, содержащая размер и положение окна, которые будут использоваться для отображения активированные сообщения.</span><span class="sxs-lookup"><span data-stu-id="f83d3-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f83d3-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f83d3-123">Return value</span></span>

<span data-ttu-id="f83d3-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f83d3-124">S_OK</span></span> 
  
> <span data-ttu-id="f83d3-125">Сообщение успешно активирована.</span><span class="sxs-lookup"><span data-stu-id="f83d3-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="f83d3-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f83d3-126">S_FALSE</span></span> 
  
> <span data-ttu-id="f83d3-127">Сообщение успешно активирована, но другого типа формы был открыт в процессе.</span><span class="sxs-lookup"><span data-stu-id="f83d3-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f83d3-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="f83d3-128">Remarks</span></span>

<span data-ttu-id="f83d3-129">Объекты формы вызвать метод **IMAPIViewContext::ActivateNext** для изменения какие сообщения, отображаемого для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f83d3-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="f83d3-130">Значение, переданное в параметре _ulDir_ указывает, какие сообщения следует был активирован и, в некоторых случаях, почему.</span><span class="sxs-lookup"><span data-stu-id="f83d3-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="f83d3-131">Флаги VCDIR_NEXT и VCDIR_PREVIOUS соответствуют пользователям, выбрав команду **следующий** или **Предыдущий** в представлении, соответственно.</span><span class="sxs-lookup"><span data-stu-id="f83d3-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="f83d3-132">Эти операции обычно соответствуют Перемещение вверх или вниз одного сообщения в форме просмотра списка сообщений.</span><span class="sxs-lookup"><span data-stu-id="f83d3-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="f83d3-133">VCDIR_DELETE VCDIR_MOVE установлены флаги и методами [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) и [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="f83d3-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="f83d3-134">Реализации этих методов вызовите **ActivateNext** с соответствующие направление и затем выполнить запрошенную операцию в окне сообщения, если выполнены **ActivateNext** звонок.</span><span class="sxs-lookup"><span data-stu-id="f83d3-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="f83d3-135">Средства просмотра формы обычно позволяют пользователям указать направление для перемещения в списке сообщений.</span><span class="sxs-lookup"><span data-stu-id="f83d3-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f83d3-136">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f83d3-136">Notes to implementers</span></span>

<span data-ttu-id="f83d3-137">Реализация [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) предоставляет следующий или предыдущий сообщение в папке, в зависимости от _ulDir_, текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f83d3-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="f83d3-138">После возврата **ActivateNext** , вызовите [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) для получения указателя на вновь активированных сообщение.</span><span class="sxs-lookup"><span data-stu-id="f83d3-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f83d3-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f83d3-139">Notes to callers</span></span>

<span data-ttu-id="f83d3-140">Если **ActivateNext** возвращает S_FALSE или текущего сообщения не указан, процедура вашей стандартного завершения работы которого следует включить вызов метода [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) формы.</span><span class="sxs-lookup"><span data-stu-id="f83d3-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="f83d3-141">Если отображается следующий или предыдущий сообщение, используйте окно прямоугольника, переданной в параметре _prcPosRect_ для его отображения.</span><span class="sxs-lookup"><span data-stu-id="f83d3-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f83d3-142">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f83d3-142">MFCMAPI reference</span></span>

<span data-ttu-id="f83d3-143">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f83d3-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f83d3-144">**����**</span><span class="sxs-lookup"><span data-stu-id="f83d3-144">**File**</span></span>|<span data-ttu-id="f83d3-145">**�������**</span><span class="sxs-lookup"><span data-stu-id="f83d3-145">**Function**</span></span>|<span data-ttu-id="f83d3-146">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f83d3-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f83d3-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f83d3-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f83d3-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f83d3-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="f83d3-149">Mfcmapi (en) реализован метод **IMAPIViewContext::ActivateNext** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="f83d3-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f83d3-150">См. также</span><span class="sxs-lookup"><span data-stu-id="f83d3-150">See also</span></span>

- [<span data-ttu-id="f83d3-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="f83d3-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="f83d3-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f83d3-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="f83d3-153">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f83d3-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

