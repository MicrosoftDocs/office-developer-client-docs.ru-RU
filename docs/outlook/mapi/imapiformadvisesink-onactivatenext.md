---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808881"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="fa4be-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="fa4be-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="fa4be-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa4be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa4be-105">Указывает, является ли форма может обрабатывать класса сообщений для следующего сообщения для отображения.</span><span class="sxs-lookup"><span data-stu-id="fa4be-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fa4be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa4be-106">Parameters</span></span>

 <span data-ttu-id="fa4be-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="fa4be-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="fa4be-108">[in] Указатель на класс сообщения следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa4be-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="fa4be-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="fa4be-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="fa4be-110">[in] Битовой маски флагов клиента или поставщика, скопированные из следующего сообщения для отображения, свойство **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)), который предоставляет сведения о состоянии содержимого таблицы, что это сообщение будет включена в.</span><span class="sxs-lookup"><span data-stu-id="fa4be-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="fa4be-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="fa4be-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="fa4be-112">[in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) следующего сообщения для отображения, который показывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa4be-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="fa4be-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="fa4be-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="fa4be-114">[out] Указатель на указатель на реализацию [IPersistMessage](ipersistmessageiunknown.md) для объекта формы, используются для новой формы, если требуется новая форма.</span><span class="sxs-lookup"><span data-stu-id="fa4be-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="fa4be-115">Могут быть возвращены указатель на значение NULL, если текущий объект формы можно использовать для отображения и сохраните следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="fa4be-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa4be-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="fa4be-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="fa4be-117">S_OK</span></span> 
  
> <span data-ttu-id="fa4be-118">Уведомление успешно и формы можно обработать следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="fa4be-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="fa4be-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fa4be-119">S_FALSE</span></span> 
  
> <span data-ttu-id="fa4be-120">Форма не обрабатывает класса сообщений для следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa4be-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa4be-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="fa4be-121">Remarks</span></span>

<span data-ttu-id="fa4be-122">Средства просмотра форм вызовите метод **IMAPIFormAdviseSink::OnActivateNext** помогут определить, является ли он может отображать следующее сообщение в папке формы.</span><span class="sxs-lookup"><span data-stu-id="fa4be-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="fa4be-123">Следующее сообщение может быть сообщение любого класса, но обычно это же класс или связанных с ними класса.</span><span class="sxs-lookup"><span data-stu-id="fa4be-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="fa4be-124">Это делает процесс чтения несколько сообщений того же класса более эффективным, включив клиентских приложений для повторного использования объекты формы, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="fa4be-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="fa4be-125">Большинство объектов формы будет использоваться класс сообщения, на который указывает параметр _lpszMessageClass_ для определения, является ли они могут обрабатывать следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="fa4be-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="fa4be-126">Обычно формы может обрабатывать сообщения, которые принадлежат классам подкласс, в дополнение к сообщениям, которые относятся к классу по умолчанию которых является класс формы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa4be-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="fa4be-127">Тем не менее формы можно использовать для определения без вопрос ли сообщение может обрабатывать, такие как состояние отправленные и неотправленные следующего сообщения других факторов.</span><span class="sxs-lookup"><span data-stu-id="fa4be-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fa4be-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="fa4be-128">Notes to implementers</span></span>

<span data-ttu-id="fa4be-129">Возвращает значение S_OK и NULL в параметре _ppPersistMessage_ , если форма может обрабатывать класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa4be-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="fa4be-130">Если форма можно создать новую форму, которая может обрабатывать сообщения, форма не может обработать, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fa4be-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="fa4be-131">Вызов фабрики класса формы для создания экземпляра объекта формы.</span><span class="sxs-lookup"><span data-stu-id="fa4be-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="fa4be-132">Сохраните этот экземпляр в содержимое параметра указатель _ppPersistMessage_ .</span><span class="sxs-lookup"><span data-stu-id="fa4be-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="fa4be-133">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="fa4be-133">Return S_OK.</span></span>
    
<span data-ttu-id="fa4be-134">Средство просмотра формы будут загружать сообщения с помощью метода [IPersistMessage::Load](ipersistmessage-load.md) , к которой принадлежит объект, на который указывает _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="fa4be-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="fa4be-135">Если ни форма, ни форму, можно создать может обрабатывать следующее сообщение, возвращает S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="fa4be-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="fa4be-136">Тем не менее как правило, формы должен не возвращаемое это значение, так как он вызывает снижению производительности в средстве просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="fa4be-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fa4be-137">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="fa4be-137">MFCMAPI reference</span></span>

<span data-ttu-id="fa4be-138">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="fa4be-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fa4be-139">**����**</span><span class="sxs-lookup"><span data-stu-id="fa4be-139">**File**</span></span>|<span data-ttu-id="fa4be-140">**�������**</span><span class="sxs-lookup"><span data-stu-id="fa4be-140">**Function**</span></span>|<span data-ttu-id="fa4be-141">**�����������**</span><span class="sxs-lookup"><span data-stu-id="fa4be-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa4be-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fa4be-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fa4be-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="fa4be-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="fa4be-144">Mfcmapi (en) использует метод **IMAPIFormAdviseSink::OnActivateNext** для реализации метода [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="fa4be-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa4be-145">См. также</span><span class="sxs-lookup"><span data-stu-id="fa4be-145">See also</span></span>



[<span data-ttu-id="fa4be-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="fa4be-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="fa4be-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa4be-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="fa4be-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="fa4be-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="fa4be-149">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="fa4be-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="fa4be-150">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="fa4be-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="fa4be-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa4be-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="fa4be-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="fa4be-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

