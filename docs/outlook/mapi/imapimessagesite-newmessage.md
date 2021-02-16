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
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438773"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="a23c1-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="a23c1-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="a23c1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a23c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a23c1-105">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a23c1-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a23c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a23c1-106">Parameters</span></span>

 <span data-ttu-id="a23c1-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="a23c1-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="a23c1-108">[in] Указывает, в какой папке должно быть составлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="a23c1-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="a23c1-109">Если переменная имеет значение FALSE, параметр  _pFolderFocus_ игнорируется, и просмотр формы может создать сообщение в любой папке.</span><span class="sxs-lookup"><span data-stu-id="a23c1-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="a23c1-110">Если переменная имеет значение TRUE и в параметре  _pFolderFocus_ передается значение NULL, сообщение будет составлено в текущей папке.</span><span class="sxs-lookup"><span data-stu-id="a23c1-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="a23c1-111">Если переменная имеет значение TRUE и в _pFolderFocus_ передается значение, не состоящее из NULL, сообщение состоит из папки, на который указывает _pFolderFocus._</span><span class="sxs-lookup"><span data-stu-id="a23c1-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="a23c1-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="a23c1-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="a23c1-113">[in] Указатель на папку, в которой создается новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a23c1-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="a23c1-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="a23c1-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="a23c1-115">[in] Указатель на объект формы для новой формы.</span><span class="sxs-lookup"><span data-stu-id="a23c1-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="a23c1-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="a23c1-116">_ppMessage_</span></span>
  
> <span data-ttu-id="a23c1-117">[out] Указатель на указатель на новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a23c1-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="a23c1-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="a23c1-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="a23c1-119">[out] Указатель на указатель на объект сайта сообщения для нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="a23c1-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="a23c1-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="a23c1-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="a23c1-121">[out] Указатель на указатель на контекст представления, который подходит для передачи в новую форму с новым сообщением.</span><span class="sxs-lookup"><span data-stu-id="a23c1-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="a23c1-122">Если форма реализует собственный контекст представления, в  _параметре ppViewContext_ можно передать NULL.</span><span class="sxs-lookup"><span data-stu-id="a23c1-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a23c1-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a23c1-123">Return value</span></span>

<span data-ttu-id="a23c1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a23c1-124">S_OK</span></span> 
  
> <span data-ttu-id="a23c1-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a23c1-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a23c1-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="a23c1-126">Remarks</span></span>

<span data-ttu-id="a23c1-127">Объекты форм вызывать метод **IMAPIMessageSite::NewMessage** для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="a23c1-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="a23c1-128">Форма использует **NewMessage** для получения нового сообщения и связанного сайта сообщений из своего представления.</span><span class="sxs-lookup"><span data-stu-id="a23c1-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="a23c1-129">Затем оно может изменить новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a23c1-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="a23c1-130">Вы также можете получить связанный контекст представления, передав в  _параметре ppViewContext_ значение, не связанное с NULL.</span><span class="sxs-lookup"><span data-stu-id="a23c1-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="a23c1-131">Этот контекст представления можно использовать напрямую или агрегировать и передавать в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a23c1-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="a23c1-132">Если требуется полная реализация, передав NULL в _ppViewContext._</span><span class="sxs-lookup"><span data-stu-id="a23c1-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="a23c1-133">Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="a23c1-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a23c1-134">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a23c1-134">MFCMAPI reference</span></span>

<span data-ttu-id="a23c1-135">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a23c1-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a23c1-136">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a23c1-136">**File**</span></span>|<span data-ttu-id="a23c1-137">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a23c1-137">**Function**</span></span>|<span data-ttu-id="a23c1-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a23c1-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a23c1-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a23c1-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a23c1-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="a23c1-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="a23c1-141">MFCMAPI использует метод **IMAPIMessageSite::NewMessage** для создания нового сообщения, создания нового представления формы и вызова **SetPersist,** чтобы настроить сообщение для просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="a23c1-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="a23c1-142">Наконец, оно возвращает просмотр формы в качестве сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="a23c1-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a23c1-143">См. также</span><span class="sxs-lookup"><span data-stu-id="a23c1-143">See also</span></span>



[<span data-ttu-id="a23c1-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a23c1-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="a23c1-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a23c1-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a23c1-146">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="a23c1-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a23c1-147">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="a23c1-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

