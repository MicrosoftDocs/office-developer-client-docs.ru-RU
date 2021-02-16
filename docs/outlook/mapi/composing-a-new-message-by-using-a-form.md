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
# <a name="composing-a-new-message-by-using-a-form"></a>Создать сообщение с помощью формы

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы использовать форму для создания нового сообщения, сначала создайте новый пользовательский объект сообщения.
  
 **Чтобы создать новое сообщение с помощью формы**
  
1. Вызовите метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) диспетчера форм, чтобы получить указатель на информационный объект формы — объект, который реализует [интерфейс IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
2. Передайте указатель в информационный объект формы в вызове [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) **CreateForm** загружает соответствующий сервер форм. Кроме того, передайте идентификатор интерфейса **в CreateForm,** чтобы указать интерфейс, который будет использоваться для доступа к новому сообщению. Обычно [IPersistMessage : IUnknown](ipersistmessageiunknown.md) запрашивается путем передачи IID_IPersistMessage **в CreateForm.**
    
3. Сохраните новое сообщение, вызывая метод [IPersistMessage::Save.](ipersistmessage-save.md) Сервер форм должен устанавливать значения для необходимых свойств сообщения при его создании. 
    
4. Загрузив сообщение с помощью одной из двух стратегий: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) или [IMAPISession::P repareForm,](imapisession-prepareform.md) за которым следует [IMAPISession::ShowForm.](imapisession-showform.md) Дополнительные сведения об этих стратегиях см. в [загружаемом сообщении в форму.](loading-a-message-into-a-form.md)
    
> [!NOTE]
> При загрузке нового настраиваемого сообщения на сервер форм существуют возможности для увеличения производительности, так как у вас уже будет возможность получить некоторые сведения о сообщении ( например, его класс) во время обработки, необходимой для вызовов **ResolveMessageClass** и **CreateForm.** По этой причине вы сможете упростить обработку, необходимую перед вызовом LoadForm над темой **LoadForm,** описанной в разделе "Загрузка сообщения [в форму".](loading-a-message-into-a-form.md) 
  

