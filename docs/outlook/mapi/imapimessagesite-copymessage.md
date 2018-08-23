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
ms.openlocfilehash: 074a806a710ce8c11adba815951c93c25d8cae7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579258"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="a1796-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="a1796-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="a1796-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1796-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1796-105">Копирует текущего сообщения в папку.</span><span class="sxs-lookup"><span data-stu-id="a1796-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="a1796-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1796-106">Parameters</span></span>

 <span data-ttu-id="a1796-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="a1796-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="a1796-108">[in] Указатель на папку, где Копировать сообщение.</span><span class="sxs-lookup"><span data-stu-id="a1796-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1796-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a1796-109">Return value</span></span>

<span data-ttu-id="a1796-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a1796-110">S_OK</span></span> 
  
> <span data-ttu-id="a1796-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a1796-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a1796-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a1796-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a1796-113">Операция не поддерживается на этом сайте сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1796-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1796-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1796-114">Remarks</span></span>

<span data-ttu-id="a1796-115">Объекты формы вызовите метод **IMAPIMessageSite::CopyMessage** для копирования текущего сообщения в новую папку.</span><span class="sxs-lookup"><span data-stu-id="a1796-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="a1796-116">**CopyMessage** не изменяет сообщение, в настоящее время отображается для пользователя и интерфейс для только что созданный сообщения не возвращаются в форму.</span><span class="sxs-lookup"><span data-stu-id="a1796-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a1796-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a1796-117">Notes to implementers</span></span>

<span data-ttu-id="a1796-118">Типичное использование метода **CopyMessage** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="a1796-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="a1796-119">Создание сообщения для текущего сообщения для копирования.</span><span class="sxs-lookup"><span data-stu-id="a1796-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="a1796-120">Вызывает метод [IPersistMessage::Save](ipersistmessage-save.md) с указатель на новое сообщение в параметре _pMessage_ и значение FALSE в параметре _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="a1796-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="a1796-121">Вызывает метод [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , передав NULL в параметре _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="a1796-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="a1796-122">Вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1796-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="a1796-123">Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a1796-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1796-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="a1796-124">MFCMAPI reference</span></span>

<span data-ttu-id="a1796-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="a1796-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1796-126">**����**</span><span class="sxs-lookup"><span data-stu-id="a1796-126">**File**</span></span>|<span data-ttu-id="a1796-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="a1796-127">**Function**</span></span>|<span data-ttu-id="a1796-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="a1796-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1796-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a1796-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a1796-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="a1796-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="a1796-131">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="a1796-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1796-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a1796-132">See also</span></span>



[<span data-ttu-id="a1796-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a1796-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a1796-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="a1796-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="a1796-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="a1796-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="a1796-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1796-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a1796-137">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a1796-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a1796-138">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="a1796-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

