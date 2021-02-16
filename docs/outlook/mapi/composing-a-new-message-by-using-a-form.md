---
title: Создать сообщение с помощью формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412802"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="c4d4f-103">Создать сообщение с помощью формы</span><span class="sxs-lookup"><span data-stu-id="c4d4f-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="c4d4f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d4f-105">Чтобы использовать форму для создания нового сообщения, сначала создайте новый пользовательский объект сообщения.</span><span class="sxs-lookup"><span data-stu-id="c4d4f-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="c4d4f-106">**Чтобы создать новое сообщение с помощью формы**</span><span class="sxs-lookup"><span data-stu-id="c4d4f-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="c4d4f-107">Вызовите метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) диспетчера форм, чтобы получить указатель на информационный объект формы — объект, который реализует [интерфейс IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4f-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="c4d4f-108">Передайте указатель в информационный объект формы в вызове [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4f-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="c4d4f-109">**CreateForm** загружает соответствующий сервер форм.</span><span class="sxs-lookup"><span data-stu-id="c4d4f-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="c4d4f-110">Кроме того, передайте идентификатор интерфейса **в CreateForm,** чтобы указать интерфейс, который будет использоваться для доступа к новому сообщению.</span><span class="sxs-lookup"><span data-stu-id="c4d4f-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="c4d4f-111">Обычно [IPersistMessage : IUnknown](ipersistmessageiunknown.md) запрашивается путем передачи IID_IPersistMessage **в CreateForm.**</span><span class="sxs-lookup"><span data-stu-id="c4d4f-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="c4d4f-112">Сохраните новое сообщение, вызывая метод [IPersistMessage::Save.](ipersistmessage-save.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4f-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="c4d4f-113">Сервер форм должен устанавливать значения для необходимых свойств сообщения при его создании.</span><span class="sxs-lookup"><span data-stu-id="c4d4f-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="c4d4f-114">Загрузив сообщение с помощью одной из двух стратегий: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) или [IMAPISession::P repareForm,](imapisession-prepareform.md) за которым следует [IMAPISession::ShowForm.](imapisession-showform.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4f-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="c4d4f-115">Дополнительные сведения об этих стратегиях см. в [загружаемом сообщении в форму.](loading-a-message-into-a-form.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4f-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="c4d4f-116">При загрузке нового настраиваемого сообщения на сервер форм существуют возможности для увеличения производительности, так как у вас уже будет возможность получить некоторые сведения о сообщении ( например, его класс) во время обработки, необходимой для вызовов **ResolveMessageClass** и **CreateForm.**</span><span class="sxs-lookup"><span data-stu-id="c4d4f-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="c4d4f-117">По этой причине вы сможете упростить обработку, необходимую перед вызовом LoadForm над темой **LoadForm,** описанной в разделе "Загрузка сообщения [в форму".](loading-a-message-into-a-form.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4f-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

