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
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335128"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="f73d4-103">Составление нового сообщения с помощью формы</span><span class="sxs-lookup"><span data-stu-id="f73d4-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="f73d4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f73d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f73d4-105">Чтобы использовать форму для создания нового сообщения, сначала создайте новый объект настраиваемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f73d4-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="f73d4-106">**Создание нового сообщения с помощью формы**</span><span class="sxs-lookup"><span data-stu-id="f73d4-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="f73d4-107">ВыЗовите метод [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) диспетчера форм, чтобы получить указатель на объект информации формы — объект, реализующий интерфейс [имапиформинфо: IMAPIProp](imapiforminfoimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="f73d4-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="f73d4-108">Передайте указатель на объект сведений о форме в вызове [имапиформмгр:: креатеформ](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="f73d4-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="f73d4-109">**Креатеформ** загружает соответствующий сервер форм.</span><span class="sxs-lookup"><span data-stu-id="f73d4-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="f73d4-110">Кроме того, передайте идентификатор интерфейса **креатеформ** , чтобы указать интерфейс, который будет использоваться для доступа к новому сообщению.</span><span class="sxs-lookup"><span data-stu-id="f73d4-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="f73d4-111">Как правило, вы запрашиваете [иперсистмессаже: IUnknown](ipersistmessageiunknown.md) , передавая Иид_иперсистмессаже в **креатеформ**.</span><span class="sxs-lookup"><span data-stu-id="f73d4-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="f73d4-112">Сохраните новое сообщение, вызвав его метод [иперсистмессаже:: Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="f73d4-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="f73d4-113">При создании сообщения сервер форм должен задавать значения для обязательных свойств сообщения.</span><span class="sxs-lookup"><span data-stu-id="f73d4-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="f73d4-114">Загрузите сообщение с помощью одной из двух стратегий: [имапиформмгр:: лоадформ](imapiformmgr-loadform.md) или [IMAPISession::P репареформ](imapisession-prepareform.md) , за которым следует [IMAPISession:: шовформ](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="f73d4-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="f73d4-115">Дополнительные сведения об этих стратегиях приведены [в статье Загрузка сообщения в форму](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="f73d4-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="f73d4-116">При загрузке нового настраиваемого сообщения на сервер форм существуют возможности для повышения производительности, так как у вас уже есть возможность получить некоторую информацию о сообщении, например его класс Message, в процессе обработки, необходимой для \*\* Вызовы Ресолвемессажекласс\*\* и **креатеформ** .</span><span class="sxs-lookup"><span data-stu-id="f73d4-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="f73d4-117">Из-за этого вы сможете упростить обработку, которую необходимо выполнить перед вызовом **лоадформ** , как описано в разделе [Загрузка сообщения в форму](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="f73d4-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

