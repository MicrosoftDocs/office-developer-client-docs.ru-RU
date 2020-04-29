---
title: имапимессажеситеделетемессаже
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321415"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="9dec2-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="9dec2-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="9dec2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dec2-105">Удаляет текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="9dec2-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="9dec2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dec2-106">Parameters</span></span>

 <span data-ttu-id="9dec2-107">_пвиевконтекст_</span><span class="sxs-lookup"><span data-stu-id="9dec2-107">_pViewContext_</span></span>
  
> <span data-ttu-id="9dec2-108">возврата Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="9dec2-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="9dec2-109">_пркпосрект_</span><span class="sxs-lookup"><span data-stu-id="9dec2-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="9dec2-110">возврата Указатель на структуру [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) , которая содержит размер и положение окна текущей формы.</span><span class="sxs-lookup"><span data-stu-id="9dec2-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="9dec2-111">В следующей отображаемой форме также используется этот прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="9dec2-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9dec2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dec2-112">Return value</span></span>

<span data-ttu-id="9dec2-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9dec2-113">S_OK</span></span> 
  
> <span data-ttu-id="9dec2-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9dec2-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9dec2-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9dec2-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9dec2-116">Эта операция не поддерживается этим сайтом сообщений.</span><span class="sxs-lookup"><span data-stu-id="9dec2-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9dec2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="9dec2-117">Remarks</span></span>

<span data-ttu-id="9dec2-118">Объект Form вызывает метод **имапимессажесите::D елетемессаже** , чтобы удалить сообщение, отображаемое в данный момент в форме.</span><span class="sxs-lookup"><span data-stu-id="9dec2-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9dec2-119">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9dec2-119">Notes to callers</span></span>

<span data-ttu-id="9dec2-120">После возврата **DeleteMessage**объекты формы должны проверять новое сообщение, а затем отменять себя, если они не существуют.</span><span class="sxs-lookup"><span data-stu-id="9dec2-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="9dec2-121">Чтобы определить, было ли сообщение **DeleteMessage** Message on Deleted или перемещено в папку " **Удаленные** ", объект формы может вызвать метод [имапимессажесите:: жетситестатус](imapimessagesite-getsitestatus.md) , чтобы определить, был ли возвращен флаг DELETE_IS_MOVE.</span><span class="sxs-lookup"><span data-stu-id="9dec2-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9dec2-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9dec2-122">Notes to implementers</span></span>

<span data-ttu-id="9dec2-123">Если реализация метода **DeleteMessage** в средстве просмотра формы перемещается к следующему сообщению после удаления сообщения, реализация должна вызвать метод [Имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md) и перед выполнением фактического удаления передать флаг VCDIR_DELETE.</span><span class="sxs-lookup"><span data-stu-id="9dec2-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="9dec2-124">Если при реализации **DeleteMessage** в средстве просмотра формы перемещается удаленное сообщение (например, в папку " **Удаленные** "), реализация должна сохранять изменения в сообщении, если сообщение было изменено.</span><span class="sxs-lookup"><span data-stu-id="9dec2-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="9dec2-125">Типичная реализация **DeleteMessage** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="9dec2-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="9dec2-126">Если реализация перемещает сообщение, оно вызывает метод [иперсистмессаже:: Save](ipersistmessage-save.md) , передавая **значение NULL** в параметре _пмессаже_ , и **значение true** в параметре _фсамеаслоад_ .</span><span class="sxs-lookup"><span data-stu-id="9dec2-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="9dec2-127">Он вызывает метод **имапивиевконтекст:: активатенекст** , передавая флаг VCDIR_DELETE в параметре _улдир_ .</span><span class="sxs-lookup"><span data-stu-id="9dec2-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="9dec2-128">Если произойдет сбой вызова **активатенекст** , возвращается значение.</span><span class="sxs-lookup"><span data-stu-id="9dec2-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="9dec2-129">Если **активатенекст** возвращает S_FALSE, вызывается метод [Иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="9dec2-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="9dec2-130">Он удаляет или перемещает сообщение.</span><span class="sxs-lookup"><span data-stu-id="9dec2-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="9dec2-131">Чтобы получить структуру **Rect** , используемую окном формы, вызовите функцию Windows [жетвиндоврект](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="9dec2-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="9dec2-132">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9dec2-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9dec2-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9dec2-133">MFCMAPI reference</span></span>

<span data-ttu-id="9dec2-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9dec2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9dec2-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9dec2-135">**File**</span></span>|<span data-ttu-id="9dec2-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9dec2-136">**Function**</span></span>|<span data-ttu-id="9dec2-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9dec2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9dec2-138">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="9dec2-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9dec2-139">Кмимапиформвиевер::D Елетемессаже</span><span class="sxs-lookup"><span data-stu-id="9dec2-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="9dec2-140">Не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9dec2-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9dec2-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9dec2-141">See also</span></span>



[<span data-ttu-id="9dec2-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="9dec2-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="9dec2-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="9dec2-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="9dec2-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="9dec2-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="9dec2-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="9dec2-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="9dec2-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9dec2-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="9dec2-147">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="9dec2-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9dec2-148">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="9dec2-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

