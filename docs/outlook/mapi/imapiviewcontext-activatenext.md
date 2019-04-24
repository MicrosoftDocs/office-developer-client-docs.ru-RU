---
title: Имапивиевконтекстактиватенекст
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351158"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="68ee2-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="68ee2-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="68ee2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68ee2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68ee2-105">Активирует следующее или предыдущее сообщение в порядке просмотра.</span><span class="sxs-lookup"><span data-stu-id="68ee2-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="68ee2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68ee2-106">Parameters</span></span>

<span data-ttu-id="68ee2-107">_Улдир_</span><span class="sxs-lookup"><span data-stu-id="68ee2-107">_ulDir_</span></span>
  
> <span data-ttu-id="68ee2-108">возврата Флаги состояния, которые предоставляют сведения о сообщении, которое необходимо активировать.</span><span class="sxs-lookup"><span data-stu-id="68ee2-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="68ee2-109">Допустимые параметры флагов:</span><span class="sxs-lookup"><span data-stu-id="68ee2-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="68ee2-110">ВКДИР_КАТЕГОРИ: средство просмотра должно активировать сообщение в другой категории представления.</span><span class="sxs-lookup"><span data-stu-id="68ee2-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="68ee2-111">Активируемое сообщение:</span><span class="sxs-lookup"><span data-stu-id="68ee2-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="68ee2-112">Первое сообщение в категории "в следующем представлении", если этот флаг имеет значение **или**ED с вкдир_некст.</span><span class="sxs-lookup"><span data-stu-id="68ee2-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="68ee2-113">Последнее сообщение в предыдущей категории представления, если этот флаг имеет значение **или**ED с вкдир_прев, а предыдущая категория развернута.</span><span class="sxs-lookup"><span data-stu-id="68ee2-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="68ee2-114">Первое сообщение в предыдущей категории представления, если этот флаг имеет значение **или**ED с вкдир_прев, а предыдущая категория не развернута.</span><span class="sxs-lookup"><span data-stu-id="68ee2-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="68ee2-115">В этом случае предыдущая категория перестанет автоматически расширяться.</span><span class="sxs-lookup"><span data-stu-id="68ee2-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="68ee2-116">ВКДИР_ДЕЛЕТЕ: средство просмотра должно активировать следующее или предыдущее сообщение, так как текущее сообщение было удалено.</span><span class="sxs-lookup"><span data-stu-id="68ee2-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="68ee2-117">ВКДИР_МОВЕ: средство просмотра должно активировать следующее или предыдущее сообщение, так как текущее сообщение было перемещено.</span><span class="sxs-lookup"><span data-stu-id="68ee2-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="68ee2-118">ВКДИР_НЕКСТ: средство просмотра должно активировать следующее сообщение в порядке просмотра.</span><span class="sxs-lookup"><span data-stu-id="68ee2-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="68ee2-119">ВКДИР_ПРЕВ: средство просмотра должно активировать предыдущее сообщение в порядке просмотра.</span><span class="sxs-lookup"><span data-stu-id="68ee2-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="68ee2-120">ВКДИР_УНРЕАД: средство просмотра должно активировать следующее или предыдущее непрочитанное сообщение в порядке просмотра.</span><span class="sxs-lookup"><span data-stu-id="68ee2-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="68ee2-121">_Пркпосрект_</span><span class="sxs-lookup"><span data-stu-id="68ee2-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="68ee2-122">возврата Указатель на структуру **прямоугольника** Windows, содержащую размер и положение окна, которое будет использоваться для отображения активированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="68ee2-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68ee2-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68ee2-123">Return value</span></span>

<span data-ttu-id="68ee2-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="68ee2-124">S_OK</span></span> 
  
> <span data-ttu-id="68ee2-125">Сообщение успешно активировано.</span><span class="sxs-lookup"><span data-stu-id="68ee2-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="68ee2-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="68ee2-126">S_FALSE</span></span> 
  
> <span data-ttu-id="68ee2-127">Сообщение успешно активировано, но в процессе открыт другой тип формы.</span><span class="sxs-lookup"><span data-stu-id="68ee2-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68ee2-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="68ee2-128">Remarks</span></span>

<span data-ttu-id="68ee2-129">Объекты форм вызовите метод **имапивиевконтекст:: активатенекст** , чтобы изменить сообщение, отображаемое для пользователя.</span><span class="sxs-lookup"><span data-stu-id="68ee2-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="68ee2-130">Значение, передаваемое в параметре _улдир_ , указывает, какое сообщение должно быть активировано, а в некоторых случаях — почему.</span><span class="sxs-lookup"><span data-stu-id="68ee2-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="68ee2-131">Флаги ВКДИР_НЕКСТ и ВКДИР_ПРЕВИАУС соответствуют пользователям, которые выбирая **следующую** или **предыдущую** команду в представлении соответственно.</span><span class="sxs-lookup"><span data-stu-id="68ee2-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="68ee2-132">Эти операции обычно соответствуют перемещению вверх или вниз одного сообщения в списке сообщений в средстве просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="68ee2-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="68ee2-133">Флаги ВКДИР_ДЕЛЕТЕ и ВКДИР_МОВЕ задаются методами [имапимессажесите::D елетемессаже](imapimessagesite-deletemessage.md) и [Имапимессажесите:: мовемессаже](imapimessagesite-movemessage.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="68ee2-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="68ee2-134">Реализации этих методов вызывают **активатенекст** с соответствующим направлением, а затем выполняют запрошенную операцию над сообщением, если не удалось вызвать **активатенекст** .</span><span class="sxs-lookup"><span data-stu-id="68ee2-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="68ee2-135">Средства просмотра форм обычно позволяют пользователям указать направление перемещения в списке сообщений.</span><span class="sxs-lookup"><span data-stu-id="68ee2-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="68ee2-136">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="68ee2-136">Notes to implementers</span></span>

<span data-ttu-id="68ee2-137">Реализация [имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md) создает следующее или предыдущее сообщение в папке в зависимости от значения свойства _улдир_, текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="68ee2-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="68ee2-138">После возврата **активатенекст** вызовите [имапимессажесите::.](imapimessagesite-getmessage.md) Get, чтобы получить указатель на вновь активируемое сообщение.</span><span class="sxs-lookup"><span data-stu-id="68ee2-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="68ee2-139">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="68ee2-139">Notes to callers</span></span>

<span data-ttu-id="68ee2-140">Если **активатенекст** возвращает S_FALSE или текущее сообщение отсутствует, выполните процедуру нормального завершения работы, которая должна включать вызов метода [Имапиформ:: шутдовнформ](imapiform-shutdownform.md) формы.</span><span class="sxs-lookup"><span data-stu-id="68ee2-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="68ee2-141">Если отображается следующее или предыдущее сообщение, используйте прямоугольник окна, переданный в параметре _пркпосрект_ , чтобы отобразить его.</span><span class="sxs-lookup"><span data-stu-id="68ee2-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="68ee2-142">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="68ee2-142">MFCMAPI reference</span></span>

<span data-ttu-id="68ee2-143">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="68ee2-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="68ee2-144">**Файл**</span><span class="sxs-lookup"><span data-stu-id="68ee2-144">**File**</span></span>|<span data-ttu-id="68ee2-145">**Функция**</span><span class="sxs-lookup"><span data-stu-id="68ee2-145">**Function**</span></span>|<span data-ttu-id="68ee2-146">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="68ee2-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68ee2-147">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="68ee2-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="68ee2-148">Кмимапиформвиевер:: Активатенекст</span><span class="sxs-lookup"><span data-stu-id="68ee2-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="68ee2-149">MFCMAPI реализует метод **имапивиевконтекст:: активатенекст** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="68ee2-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68ee2-150">См. также</span><span class="sxs-lookup"><span data-stu-id="68ee2-150">See also</span></span>

- [<span data-ttu-id="68ee2-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="68ee2-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="68ee2-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68ee2-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="68ee2-153">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="68ee2-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

