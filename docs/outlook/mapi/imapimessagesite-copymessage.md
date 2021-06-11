---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430002"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="54501-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="54501-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="54501-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54501-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54501-105">Копирует текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="54501-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="54501-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="54501-106">Parameters</span></span>

 <span data-ttu-id="54501-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="54501-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="54501-108">[in] Указатель на папку, в которой должно быть скопировано сообщение.</span><span class="sxs-lookup"><span data-stu-id="54501-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54501-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54501-109">Return value</span></span>

<span data-ttu-id="54501-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="54501-110">S_OK</span></span> 
  
> <span data-ttu-id="54501-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="54501-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="54501-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="54501-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="54501-113">Операция не поддерживается на этом сайте сообщений.</span><span class="sxs-lookup"><span data-stu-id="54501-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54501-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="54501-114">Remarks</span></span>

<span data-ttu-id="54501-115">Объекты формы называют **метод IMAPIMessageSite::CopyMessage,** чтобы скопировать текущее сообщение в новую папку.</span><span class="sxs-lookup"><span data-stu-id="54501-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="54501-116">**CopyMessage** не меняет отображаемого в настоящее время сообщения пользователю, и интерфейс для вновь созданного сообщения не возвращается в форму.</span><span class="sxs-lookup"><span data-stu-id="54501-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="54501-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="54501-117">Notes to implementers</span></span>

<span data-ttu-id="54501-118">Типичная реализация метода **CopyMessage** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="54501-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="54501-119">Создает новое сообщение для копирования текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="54501-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="54501-120">Вызывает [метод IPersistMessage:::Save](ipersistmessage-save.md) с указателем на новое сообщение в _параметре pMessage_ и FALSE в _параметре fSameAsLoad._</span><span class="sxs-lookup"><span data-stu-id="54501-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="54501-121">Вызывает [метод IPersistMessage::SaveCompleted,](ipersistmessage-savecompleted.md) передавая NULL в _параметре pMessage._</span><span class="sxs-lookup"><span data-stu-id="54501-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="54501-122">Вызывает [метод IMAPIProp::SaveChanges в](imapiprop-savechanges.md) новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="54501-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="54501-123">Список интерфейсов, связанных с серверами форм, см. в перечне [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="54501-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="54501-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="54501-124">MFCMAPI reference</span></span>

<span data-ttu-id="54501-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="54501-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="54501-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="54501-126">**File**</span></span>|<span data-ttu-id="54501-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="54501-127">**Function**</span></span>|<span data-ttu-id="54501-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="54501-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54501-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="54501-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="54501-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="54501-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="54501-131">Не реализовано.</span><span class="sxs-lookup"><span data-stu-id="54501-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54501-132">См. также</span><span class="sxs-lookup"><span data-stu-id="54501-132">See also</span></span>



[<span data-ttu-id="54501-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="54501-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="54501-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="54501-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="54501-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="54501-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="54501-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54501-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="54501-137">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="54501-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="54501-138">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="54501-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

