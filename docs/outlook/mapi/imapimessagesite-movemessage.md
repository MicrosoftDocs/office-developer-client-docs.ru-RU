---
title: Имапимессажеситемовемессаже
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321367"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="130b4-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="130b4-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="130b4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="130b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="130b4-105">ПереМещает текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="130b4-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="130b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="130b4-106">Parameters</span></span>

 <span data-ttu-id="130b4-107">_Пфолдердестинатион_</span><span class="sxs-lookup"><span data-stu-id="130b4-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="130b4-108">возврата Указатель на папку, в которую перемещается сообщение.</span><span class="sxs-lookup"><span data-stu-id="130b4-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="130b4-109">_Пвиевконтекст_</span><span class="sxs-lookup"><span data-stu-id="130b4-109">_pViewContext_</span></span>
  
> <span data-ttu-id="130b4-110">возврата Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="130b4-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="130b4-111">_Пркпосрект_</span><span class="sxs-lookup"><span data-stu-id="130b4-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="130b4-112">возврата Указатель на структуру [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) , которая содержит размер и положение окна текущей формы.</span><span class="sxs-lookup"><span data-stu-id="130b4-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="130b4-113">В следующей отображаемой форме также используется этот прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="130b4-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="130b4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="130b4-114">Return value</span></span>

<span data-ttu-id="130b4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="130b4-115">S_OK</span></span> 
  
> <span data-ttu-id="130b4-116">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="130b4-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="130b4-117">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="130b4-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="130b4-118">Эта операция не поддерживается этим сайтом сообщений.</span><span class="sxs-lookup"><span data-stu-id="130b4-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="130b4-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="130b4-119">Remarks</span></span>

<span data-ttu-id="130b4-120">Объекты формы вызывают метод **имапимессажесите:: мовемессаже** для перемещения текущего сообщения в новую папку.</span><span class="sxs-lookup"><span data-stu-id="130b4-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="130b4-121">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="130b4-121">Notes to implementers</span></span>

<span data-ttu-id="130b4-122">Реализация **Мовемессаже** в средстве просмотра формы должна вызвать метод [Имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md) , передав флаг вкдир_мове, прежде чем переносить сообщение в новую папку.</span><span class="sxs-lookup"><span data-stu-id="130b4-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="130b4-123">Чтобы получить структуру **Rect** , используемую окном формы, вызовите функцию Windows [жетвиндоврект](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="130b4-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="130b4-124">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="130b4-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="130b4-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="130b4-125">Notes to callers</span></span>

<span data-ttu-id="130b4-126">После возврата **мовемессаже**формы должны проверять текущее сообщение, а затем отменять себя, если они не существуют.</span><span class="sxs-lookup"><span data-stu-id="130b4-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="130b4-127">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="130b4-127">MFCMAPI reference</span></span>

<span data-ttu-id="130b4-128">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="130b4-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="130b4-129">**Файл**</span><span class="sxs-lookup"><span data-stu-id="130b4-129">**File**</span></span>|<span data-ttu-id="130b4-130">**Функция**</span><span class="sxs-lookup"><span data-stu-id="130b4-130">**Function**</span></span>|<span data-ttu-id="130b4-131">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="130b4-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="130b4-132">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="130b4-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="130b4-133">Кмимапиформвиевер:: Мовемессаже</span><span class="sxs-lookup"><span data-stu-id="130b4-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="130b4-134">Не реализовано.</span><span class="sxs-lookup"><span data-stu-id="130b4-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="130b4-135">См. также</span><span class="sxs-lookup"><span data-stu-id="130b4-135">See also</span></span>



[<span data-ttu-id="130b4-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="130b4-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="130b4-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="130b4-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="130b4-138">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="130b4-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="130b4-139">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="130b4-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

