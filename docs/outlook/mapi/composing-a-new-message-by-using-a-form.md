---
title: Составление нового сообщения с помощью формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 667d7afe1772786507ffc8eb75f901439ada61d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587870"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="5002b-103">Составление нового сообщения с помощью формы</span><span class="sxs-lookup"><span data-stu-id="5002b-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="5002b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5002b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5002b-105">Чтобы использовать форму для создания нового сообщения, сначала необходимо создайте новый объект настраиваемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="5002b-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="5002b-106">**Чтобы создать новое сообщение с помощью формы**</span><span class="sxs-lookup"><span data-stu-id="5002b-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="5002b-107">Вызовите метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) диспетчер форм, чтобы получить указатель на объект данных формы — это объект, реализующий [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5002b-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="5002b-108">Передайте указатель мыши в объект данных формы в вызове [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="5002b-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="5002b-109">**CreateForm** загружает server соответствующую форму.</span><span class="sxs-lookup"><span data-stu-id="5002b-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="5002b-110">Кроме того передайте идентификатор интерфейса **CreateForm** для указания интерфейса, которые будут использоваться для доступа к нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="5002b-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="5002b-111">Как правило, запрос [IPersistMessage: IUnknown](ipersistmessageiunknown.md) , передав IID_IPersistMessage **CreateForm**.</span><span class="sxs-lookup"><span data-stu-id="5002b-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="5002b-112">Сохраните новые сообщения путем вызова метода [IPersistMessage::Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="5002b-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="5002b-113">Сервера форм следует задать значения для свойства необходимые сообщения при создании сообщения.</span><span class="sxs-lookup"><span data-stu-id="5002b-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="5002b-114">Загружать сообщения с помощью одного из двух стратегий: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) или [IMAPISession::PrepareForm](imapisession-prepareform.md) следуют [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="5002b-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="5002b-115">Дополнительные сведения об этих стратегий см [В форме сообщения](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="5002b-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="5002b-116">Существует возможности для повышения производительности при загрузке нового настраиваемого сообщения в форме сервера, так как возможность получить сведения о сообщении уже были применены, такие как его класса сообщений — во время обработки, необходимые для ** ResolveMessageClass** и вызывает метод **CreateForm** .</span><span class="sxs-lookup"><span data-stu-id="5002b-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="5002b-117">Таким образом вы сможете упростить обработки, требуемые до вызова **LoadForm** через, как описано в разделе [Загрузка в форме сообщения](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="5002b-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

