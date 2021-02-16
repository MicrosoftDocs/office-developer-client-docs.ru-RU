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
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411766"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="90498-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="90498-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="90498-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90498-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90498-105">Указывает, может ли форма обрабатывать класс сообщения следующего сообщения для отображения.</span><span class="sxs-lookup"><span data-stu-id="90498-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="90498-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90498-106">Parameters</span></span>

 <span data-ttu-id="90498-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="90498-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="90498-108">[in] Указатель на класс сообщения следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="90498-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="90498-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="90498-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="90498-110">[in] Битоваяmass клиентских или определяемых поставщиком флагов, скопированная из свойства **PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)следующего сообщения, которое предоставляет сведения о состоянии таблицы содержимого, в которую включено сообщение.</span><span class="sxs-lookup"><span data-stu-id="90498-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="90498-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="90498-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="90498-112">[in] Указатель на битовуюmask флагов, скопированную из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)следующего сообщения, которое будет отображаться, которое указывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="90498-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="90498-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="90498-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="90498-114">[out] Указатель на указатель на реализацию [IPersistMessage](ipersistmessageiunknown.md) для объекта формы, используемой для новой формы, если требуется новая форма.</span><span class="sxs-lookup"><span data-stu-id="90498-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="90498-115">Если текущий объект формы можно использовать для отображения и сохранения следующего сообщения, можно вернуть указатель на NULL.</span><span class="sxs-lookup"><span data-stu-id="90498-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="90498-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90498-116">Return value</span></span>

<span data-ttu-id="90498-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="90498-117">S_OK</span></span> 
  
> <span data-ttu-id="90498-118">Уведомление успешно, и форма может обработать следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="90498-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="90498-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="90498-119">S_FALSE</span></span> 
  
> <span data-ttu-id="90498-120">Форма не обрабатывает класс сообщения следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="90498-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90498-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="90498-121">Remarks</span></span>

<span data-ttu-id="90498-122">С помощью метода **IMAPIFormAdviseSink::OnActivateNext** форма может определить, может ли форма отображать следующее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="90498-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="90498-123">Следующее сообщение может быть сообщением любого класса, но обычно оно относится к одному классу или связанному классу.</span><span class="sxs-lookup"><span data-stu-id="90498-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="90498-124">Это делает процесс чтения нескольких сообщений одного класса более эффективным, позволяя клиентские приложения по возможности повторно использовать объекты форм.</span><span class="sxs-lookup"><span data-stu-id="90498-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="90498-125">Большинство объектов форм будут использовать класс сообщения, на который указывает параметр  _lpszMessageClass,_ чтобы определить, могут ли они обрабатывать следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="90498-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="90498-126">Обычно форма может обрабатывать сообщения, принадлежащие классам, класс формы по умолчанию которых является подклассом, в дополнение к сообщениям, принадлежащим к классу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90498-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="90498-127">Однако форма может использовать другие факторы, чтобы определить, можно ли обрабатывать сообщение, например, состояние "отправлено" или "не является" следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="90498-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="90498-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="90498-128">Notes to implementers</span></span>

<span data-ttu-id="90498-129">Возвращает S_OK и NULL в  _параметре ppPersistMessage,_ если форма может обрабатывать класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="90498-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="90498-130">Если форма может создать форму, которая может обрабатывать сообщение, которое не может обрабатывать форма, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="90498-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="90498-131">Вызовите фабрику классов формы, чтобы создать экземпляр нового объекта формы.</span><span class="sxs-lookup"><span data-stu-id="90498-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="90498-132">Храните этот экземпляр в содержимом параметра _указателя ppPersistMessage._</span><span class="sxs-lookup"><span data-stu-id="90498-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="90498-133">Возврат S_OK.</span><span class="sxs-lookup"><span data-stu-id="90498-133">Return S_OK.</span></span>
    
<span data-ttu-id="90498-134">Просмотр форм загрузит сообщение с помощью метода [IPersistMessage::Load,](ipersistmessage-load.md) который принадлежит объекту, на который указывает _ppPersistMessage._</span><span class="sxs-lookup"><span data-stu-id="90498-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="90498-135">Если ни форма, ни форма, которую вы можете создать, не могут обрабатывать следующее сообщение, S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="90498-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="90498-136">Однако в целом формы не должны возвращать это значение, так как это приводит к снижению производительности в представлении формы.</span><span class="sxs-lookup"><span data-stu-id="90498-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="90498-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="90498-137">MFCMAPI reference</span></span>

<span data-ttu-id="90498-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="90498-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="90498-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="90498-139">**File**</span></span>|<span data-ttu-id="90498-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="90498-140">**Function**</span></span>|<span data-ttu-id="90498-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="90498-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90498-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="90498-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="90498-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="90498-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="90498-144">MFCMAPI использует метод **IMAPIFormAdviseSink::OnActivateNext** для реализации метода [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)</span><span class="sxs-lookup"><span data-stu-id="90498-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90498-145">См. также</span><span class="sxs-lookup"><span data-stu-id="90498-145">See also</span></span>



[<span data-ttu-id="90498-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="90498-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="90498-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90498-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="90498-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="90498-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="90498-149">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="90498-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="90498-150">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="90498-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="90498-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90498-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="90498-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="90498-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

