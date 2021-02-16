---
title: Отправка и получение уведомлений формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431857"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="e4866-103">Отправка и получение уведомлений формы</span><span class="sxs-lookup"><span data-stu-id="e4866-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="e4866-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4866-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4866-105">Уведомления форм используются в MAPI для упрощения взаимодействия как из формы с вашим средством просмотра, так и с вашего средства просмотра с формой.</span><span class="sxs-lookup"><span data-stu-id="e4866-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="e4866-106">Формы отправляют уведомления вашему зрителю при одном из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="e4866-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="e4866-107">Форма закрыта.</span><span class="sxs-lookup"><span data-stu-id="e4866-107">The form is closed.</span></span>
    
- <span data-ttu-id="e4866-108">В форме загружается новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="e4866-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="e4866-109">Операция сохранения завершена.</span><span class="sxs-lookup"><span data-stu-id="e4866-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="e4866-110">Отправляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="e4866-110">A message is sent.</span></span>
    
<span data-ttu-id="e4866-111">Каждый из этих типов событий соответствует определенному методу [в IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)— одному из интерфейсов, которые должно реализовать ваше представление форм.</span><span class="sxs-lookup"><span data-stu-id="e4866-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="e4866-112">Когда происходит событие, форма вызывает соответствующий метод **IMAPIViewAdviseSink** в приемнике консультации вашего просматриваемого.</span><span class="sxs-lookup"><span data-stu-id="e4866-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="e4866-113">Например, когда поступает новое сообщение, которое ваше представление должно включить в свое отображение, форма вызывает метод [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e4866-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="e4866-114">Реализуйте тонущий совет в представлении так, чтобы это было логично для вашего зрителя; стандартная реализация не существует.</span><span class="sxs-lookup"><span data-stu-id="e4866-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="e4866-115">Например, в **OnNewMessage** можно обновить представление таблицы содержимого текущей папки, включив только что созданное сообщение.</span><span class="sxs-lookup"><span data-stu-id="e4866-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="e4866-116">В [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md)метод, который будет вызван при отправке события сообщения, можно скопировать отправленное сообщение в папку "Отправленные".</span><span class="sxs-lookup"><span data-stu-id="e4866-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="e4866-117">Формы получают уведомления от просматривающих, когда происходит изменение, которое влияет на форму, и при загрузке нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="e4866-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="e4866-118">Чтобы уведомить форму, вызовите один из методов **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) или [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="e4866-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="e4866-119">Вызовите **OnChange,** чтобы сообщить о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e4866-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="e4866-120">Например, если форма отображает последний элемент в папке при поступления нового сообщения, вызовите **OnChange** с флагом VCSTATUS_NEXT, чтобы сообщить форме, что теперь существует следующий элемент.</span><span class="sxs-lookup"><span data-stu-id="e4866-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="e4866-121">Вызовите **OnActivateNext, чтобы** предупредить форму о поступлении нового сообщения, которое может отображаться или не отображаться.</span><span class="sxs-lookup"><span data-stu-id="e4866-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="e4866-122">Передав класс сообщения в **OnActivateNext.**</span><span class="sxs-lookup"><span data-stu-id="e4866-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="e4866-123">Уведомления объектом формы для клиентского приложения обрабатываются интерфейсом **IMAPIViewAdviseSink клиентского** приложения.</span><span class="sxs-lookup"><span data-stu-id="e4866-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="e4866-124">Дополнительные сведения см. в [подразделе IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e4866-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

