---
title: IMAPIMessageSiteMoveMessage
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
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808974"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="524f4-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="524f4-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="524f4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="524f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="524f4-105">Перемещает текущего сообщения в папку.</span><span class="sxs-lookup"><span data-stu-id="524f4-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="524f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="524f4-106">Parameters</span></span>

 <span data-ttu-id="524f4-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="524f4-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="524f4-108">[in] Указатель на папку, где перемещать сообщения.</span><span class="sxs-lookup"><span data-stu-id="524f4-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="524f4-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="524f4-109">_pViewContext_</span></span>
  
> <span data-ttu-id="524f4-110">[in] Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="524f4-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="524f4-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="524f4-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="524f4-112">[in] Указатель на структуру [Прямоугольник](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) , содержащий положение и размер окна текущей формы.</span><span class="sxs-lookup"><span data-stu-id="524f4-112">[in] A pointer to a [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="524f4-113">Далее форме, отображаемой также использует этот прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="524f4-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="524f4-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="524f4-114">Return value</span></span>

<span data-ttu-id="524f4-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="524f4-115">S_OK</span></span> 
  
> <span data-ttu-id="524f4-116">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="524f4-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="524f4-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="524f4-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="524f4-118">Операция не поддерживается на этом сайте сообщения.</span><span class="sxs-lookup"><span data-stu-id="524f4-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="524f4-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="524f4-119">Remarks</span></span>

<span data-ttu-id="524f4-120">Объекты формы вызовите метод **IMAPIMessageSite::MoveMessage** для перемещения текущего сообщения в новую папку.</span><span class="sxs-lookup"><span data-stu-id="524f4-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="524f4-121">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="524f4-121">Notes to implementers</span></span>

<span data-ttu-id="524f4-122">Реализация средства просмотра формы **MoveMessage** необходимо вызвать метод [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , передав флаг VCDIR_MOVE, прежде чем фактически перемещение сообщения в новую папку.</span><span class="sxs-lookup"><span data-stu-id="524f4-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="524f4-123">Для получения структуры **Прямоугольник** , используемых окно формы, вызовите функцию Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="524f4-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="524f4-124">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="524f4-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="524f4-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="524f4-125">Notes to callers</span></span>

<span data-ttu-id="524f4-126">После возврата **MoveMessage**форм необходимо проверить для текущего сообщения и затем закрыть сами, если не существует.</span><span class="sxs-lookup"><span data-stu-id="524f4-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="524f4-127">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="524f4-127">MFCMAPI reference</span></span>

<span data-ttu-id="524f4-128">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="524f4-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="524f4-129">**����**</span><span class="sxs-lookup"><span data-stu-id="524f4-129">**File**</span></span>|<span data-ttu-id="524f4-130">**�������**</span><span class="sxs-lookup"><span data-stu-id="524f4-130">**Function**</span></span>|<span data-ttu-id="524f4-131">**�����������**</span><span class="sxs-lookup"><span data-stu-id="524f4-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="524f4-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="524f4-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="524f4-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="524f4-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="524f4-134">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="524f4-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="524f4-135">См. также</span><span class="sxs-lookup"><span data-stu-id="524f4-135">See also</span></span>



[<span data-ttu-id="524f4-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="524f4-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="524f4-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="524f4-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="524f4-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="524f4-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="524f4-139">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="524f4-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

