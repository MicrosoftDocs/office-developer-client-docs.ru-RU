---
title: Имапиформадвисесинконактиватенекст
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329437"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="3cff4-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="3cff4-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="3cff4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cff4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cff4-105">Указывает, может ли форма обрабатывать класс сообщения следующего отображаемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="3cff4-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="3cff4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cff4-106">Parameters</span></span>

 <span data-ttu-id="3cff4-107">_Лпсзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="3cff4-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="3cff4-108">возврата Указатель на класс сообщения следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3cff4-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="3cff4-109">_Улмессажестатус_</span><span class="sxs-lookup"><span data-stu-id="3cff4-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="3cff4-110">возврата Битовая маска определяемых клиентом или поставщика флагов, скопированных из свойства **пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) следующего отображаемого сообщения, которое предоставляет сведения о состоянии таблицы содержимого, в которую включено сообщение возврата.</span><span class="sxs-lookup"><span data-stu-id="3cff4-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="3cff4-111">_Улмессажефлагс_</span><span class="sxs-lookup"><span data-stu-id="3cff4-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="3cff4-112">возврата Указатель на битовую маску флагов, скопированных из свойства **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) следующего отображаемого сообщения, которое показывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="3cff4-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="3cff4-113">_Ппперсистмессаже_</span><span class="sxs-lookup"><span data-stu-id="3cff4-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="3cff4-114">вышли Указатель на указатель на реализацию [иперсистмессаже](ipersistmessageiunknown.md) для объекта формы, используемого для новой формы, если требуется новая форма.</span><span class="sxs-lookup"><span data-stu-id="3cff4-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="3cff4-115">Указатель на NULL можно вернуть, если текущий объект формы можно использовать для отображения и сохранения следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3cff4-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3cff4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cff4-116">Return value</span></span>

<span data-ttu-id="3cff4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3cff4-117">S_OK</span></span> 
  
> <span data-ttu-id="3cff4-118">Уведомление было успешным, и форма может обрабатывать следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="3cff4-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="3cff4-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3cff4-119">S_FALSE</span></span> 
  
> <span data-ttu-id="3cff4-120">Форма не обрабатывает класс сообщения следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3cff4-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3cff4-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cff4-121">Remarks</span></span>

<span data-ttu-id="3cff4-122">Средства просмотра форм вызывают метод **имапиформадвисесинк:: онактиватенекст** , чтобы определить, может ли форма отображать следующее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="3cff4-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="3cff4-123">Следующее сообщение может быть сообщением любого класса, но обычно оно относится к тому же классу или связанному классу.</span><span class="sxs-lookup"><span data-stu-id="3cff4-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="3cff4-124">Это делает процесс чтения нескольких сообщений одного класса более эффективным, позволяя клиентским приложениям повторно использовать объекты форм по мере возможности.</span><span class="sxs-lookup"><span data-stu-id="3cff4-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="3cff4-125">Большинство объектов Form будут использовать класс Message, на который указывает параметр _лпсзмессажекласс_ , чтобы определить, могут ли они обрабатывать следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="3cff4-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="3cff4-126">Как правило, форма может обрабатывать сообщения, принадлежащие классам, для которых класс формы по умолчанию является подклассом, в дополнение к сообщениям, принадлежащим классу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cff4-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="3cff4-127">Тем не менее, форма может использовать другие факторы, чтобы определить, может ли сообщение быть обработано, например состояние отправления или неотправления следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3cff4-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3cff4-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3cff4-128">Notes to implementers</span></span>

<span data-ttu-id="3cff4-129">В параметре _Ппперсистмессаже_ возвращаются значения S_OK и NULL, если форма может обрабатывать класс Message.</span><span class="sxs-lookup"><span data-stu-id="3cff4-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="3cff4-130">Если форма может создать новую форму, которая может обрабатывать сообщение, которое форма не может обработать, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3cff4-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="3cff4-131">ВыЗовите фабрику классов формы, чтобы создать экземпляр нового объекта Form.</span><span class="sxs-lookup"><span data-stu-id="3cff4-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="3cff4-132">Сохраните этот экземпляр в содержимом параметра _ппперсистмессаже_ указателя.</span><span class="sxs-lookup"><span data-stu-id="3cff4-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="3cff4-133">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="3cff4-133">Return S_OK.</span></span>
    
<span data-ttu-id="3cff4-134">Средство просмотра форм загрузит сообщение, используя метод [иперсистмессаже:: Load](ipersistmessage-load.md) , принадлежащий объекту, на который указывает _ппперсистмессаже_.</span><span class="sxs-lookup"><span data-stu-id="3cff4-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="3cff4-135">Если ни форма, ни форма, которые вы можете создать, не смогут обработать следующее сообщение, возвращается S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="3cff4-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="3cff4-136">Однако в общем случае формы не должны возвращать это значение, так как это приводит к снижению производительности в средстве просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="3cff4-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3cff4-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3cff4-137">MFCMAPI reference</span></span>

<span data-ttu-id="3cff4-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3cff4-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3cff4-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3cff4-139">**File**</span></span>|<span data-ttu-id="3cff4-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3cff4-140">**Function**</span></span>|<span data-ttu-id="3cff4-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3cff4-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3cff4-142">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="3cff4-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3cff4-143">Кмимапиформвиевер:: Активатенекст</span><span class="sxs-lookup"><span data-stu-id="3cff4-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="3cff4-144">MFCMAPI использует метод **имапиформадвисесинк:: онактиватенекст** для реализации метода [Имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="3cff4-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3cff4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="3cff4-145">See also</span></span>



[<span data-ttu-id="3cff4-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="3cff4-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="3cff4-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cff4-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="3cff4-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="3cff4-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="3cff4-149">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="3cff4-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="3cff4-150">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3cff4-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="3cff4-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cff4-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="3cff4-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3cff4-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

