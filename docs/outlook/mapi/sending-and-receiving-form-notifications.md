---
title: Отправка и получение уведомлений о формах
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7148383c92b59adb9d3783e079e7c5f28c038eac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588995"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="fdbfa-103">Отправка и получение уведомлений о формах</span><span class="sxs-lookup"><span data-stu-id="fdbfa-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="fdbfa-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdbfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdbfa-105">Уведомления о форм используются в MAPI для упрощения обмена данными и из формы к средству просмотра, так и из вашего средства просмотра в форму.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="fdbfa-106">Формы отправлять уведомления для используемого средства просмотра при возникновении одного из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="fdbfa-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="fdbfa-107">Форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-107">The form is closed.</span></span>
    
- <span data-ttu-id="fdbfa-108">Новое сообщение будет загружен в форме.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="fdbfa-109">Сохранение операция выполнена.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="fdbfa-110">Сообщение отправлено.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-110">A message is sent.</span></span>
    
<span data-ttu-id="fdbfa-111">Каждый из этих типов событий соответствуют конкретного метода в [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), один из интерфейсов, которые должен реализовывать вашей формы просмотра.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="fdbfa-112">Когда возникает событие, формы, вызывает соответствующий метод **IMAPIViewAdviseSink** в вашей просмотра 's уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="fdbfa-113">Например при получении нового сообщения, что ваше средство просмотра следует включить в его отображения, формы вызывает метод [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="fdbfa-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="fdbfa-114">Реализация представления уведомить приемник таким образом, что смысл для просмотра; отсутствует стандартный реализация.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="fdbfa-115">Например в **OnNewMessage** можно обновить представление таблицы содержимое текущей папки для включения вновь поступивших сообщений.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="fdbfa-116">В [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), метод, вызываемый при получении события отправляемого сообщения, можно скопировать отправляемого сообщения в папке "Отправленные".</span><span class="sxs-lookup"><span data-stu-id="fdbfa-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="fdbfa-117">Формы получать уведомления от используемого средства просмотра при изменении, влияющей на форме и при загрузке нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="fdbfa-118">Чтобы уведомить формы, вызовите один из методов **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) или [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="fdbfa-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="fdbfa-119">Вызова **OnChange** сообщать состояние.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="fdbfa-120">К примеру Если форма отображает последнего элемента в папке при получении нового сообщения, вызова **OnChange** с установленным флагом VCSTATUS_NEXT сообщить формы, что теперь имеется следующий элемент.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="fdbfa-121">Вызов **OnActivateNext** для оповещения формы для поступления нового сообщения, что он может или не может иметь возможность отображения.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="fdbfa-122">Передайте класса сообщений для сообщения **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="fdbfa-123">Интерфейс **IMAPIViewAdviseSink** клиентское приложение обрабатывается уведомлений с помощью объекта формы для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="fdbfa-124">Дополнительные сведения можно [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="fdbfa-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

