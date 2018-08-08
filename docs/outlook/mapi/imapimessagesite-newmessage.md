---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808978"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="54d6e-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="54d6e-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="54d6e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54d6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54d6e-105">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="54d6e-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="54d6e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54d6e-106">Parameters</span></span>

 <span data-ttu-id="54d6e-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="54d6e-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="54d6e-108">[in] Указывает, в папке, какие сообщения следует включать в себя.</span><span class="sxs-lookup"><span data-stu-id="54d6e-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="54d6e-109">Если эта переменная имеет значение FALSE, параметр _pFolderFocus_ игнорируется и просмотра формы можно создать сообщение в любой папке.</span><span class="sxs-lookup"><span data-stu-id="54d6e-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="54d6e-110">Если эта переменная имеет значение TRUE и передается в параметре _pFolderFocus_ , сообщение состоит в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="54d6e-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="54d6e-111">Если эта переменная имеет значение TRUE, НЕНУЛЕВОЕ значение передается в _pFolderFocus_сообщение состоит в папке, на который указывает _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="54d6e-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="54d6e-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="54d6e-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="54d6e-113">[in] Указатель на папку, где создается новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="54d6e-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="54d6e-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="54d6e-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="54d6e-115">[in] Указатель на объект формы для новой формы.</span><span class="sxs-lookup"><span data-stu-id="54d6e-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="54d6e-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="54d6e-116">_ppMessage_</span></span>
  
> <span data-ttu-id="54d6e-117">[out] Указатель на указатель на новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="54d6e-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="54d6e-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="54d6e-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="54d6e-119">[out] Указатель на указатель на объект сайта сообщения для нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="54d6e-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="54d6e-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="54d6e-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="54d6e-121">[out] Указатель на указатель на контекст представления, подходящую для передачи в новую форму с помощью нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="54d6e-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="54d6e-122">Если форма реализует контекст представления, NULL может быть передан в параметре _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="54d6e-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="54d6e-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="54d6e-123">Return value</span></span>

<span data-ttu-id="54d6e-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="54d6e-124">S_OK</span></span> 
  
> <span data-ttu-id="54d6e-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="54d6e-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54d6e-126">���������</span><span class="sxs-lookup"><span data-stu-id="54d6e-126">Remarks</span></span>

<span data-ttu-id="54d6e-127">Объекты формы вызовите метод **IMAPIMessageSite::NewMessage** для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="54d6e-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="54d6e-128">Форма использует **NewMessage** для получения новых сообщений и связанные сообщения сайта с его представления.</span><span class="sxs-lookup"><span data-stu-id="54d6e-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="54d6e-129">Затем можно изменить нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="54d6e-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="54d6e-130">Путем передачи НЕНУЛЕВОЕ значение с помощью параметра _ppViewContext_ может также получить контекст связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="54d6e-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="54d6e-131">В этом контексте представления можно использовать непосредственно или объединять, переданной в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="54d6e-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="54d6e-132">Если требуется полная реализация, передайте _ppViewContext_NULL.</span><span class="sxs-lookup"><span data-stu-id="54d6e-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="54d6e-133">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="54d6e-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="54d6e-134">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="54d6e-134">MFCMAPI reference</span></span>

<span data-ttu-id="54d6e-135">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="54d6e-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="54d6e-136">**����**</span><span class="sxs-lookup"><span data-stu-id="54d6e-136">**File**</span></span>|<span data-ttu-id="54d6e-137">**�������**</span><span class="sxs-lookup"><span data-stu-id="54d6e-137">**Function**</span></span>|<span data-ttu-id="54d6e-138">**�����������**</span><span class="sxs-lookup"><span data-stu-id="54d6e-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54d6e-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="54d6e-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="54d6e-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="54d6e-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="54d6e-141">Mfcmapi (en) использует метод **IMAPIMessageSite::NewMessage** для создания нового сообщения, создайте новое средство просмотра формы и вызова **SetPersist** , чтобы задать для сообщения на форму просмотра.</span><span class="sxs-lookup"><span data-stu-id="54d6e-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="54d6e-142">И, наконец он возвращает средство просмотра формы как сайт сообщения.</span><span class="sxs-lookup"><span data-stu-id="54d6e-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54d6e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="54d6e-143">See also</span></span>



[<span data-ttu-id="54d6e-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54d6e-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="54d6e-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54d6e-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="54d6e-146">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="54d6e-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="54d6e-147">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="54d6e-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

