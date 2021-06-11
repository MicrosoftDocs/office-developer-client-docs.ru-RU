---
title: Сочинение нового сообщения с помощью формы
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
# <a name="composing-a-new-message-by-using-a-form"></a>Сочинение нового сообщения с помощью формы

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы использовать форму для создания нового сообщения, сначала создайте новый настраиваемый объект сообщения.
  
 **Для составить новое сообщение с помощью формы**
  
1. Вызов метода [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для получения указателя для информационного объекта формы — объекта, реализуемого [интерфейсом IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
2. Передай указатель на информационный объект формы в [вызове в IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** загружает соответствующий сервер форм. Кроме того, передайте идентификатор интерфейса **в CreateForm,** чтобы указать интерфейс, который будет использоваться для доступа к новому сообщению. Как правило, вы [запрашиваете IPersistMessage : IUnknown,](ipersistmessageiunknown.md) передав IID_IPersistMessage **CreateForm**.
    
3. Сохраните новое сообщение, назвав метод [IPersistMessage::Save.](ipersistmessage-save.md) Сервер формы должен устанавливать значения для необходимых свойств сообщения при создании сообщения. 
    
4. Загрузив сообщение с помощью одной из двух стратегий: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) или [IMAPISession::P repareForm,](imapisession-prepareform.md) а затем [IMAPISession::ShowForm](imapisession-showform.md). Дополнительные сведения об этих стратегиях см. в сообщении [Loading a Message into a Form.](loading-a-message-into-a-form.md)
    
> [!NOTE]
> Есть возможности для увеличения производительности при загрузке нового настраиваемого сообщения на сервер формы, так как у вас уже будет возможность получить некоторую информацию о сообщении , например класс сообщения, во время обработки, необходимой для вызовов **ResolveMessageClass** и **CreateForm.** Из-за этого вы сможете упростить обработку, необходимую перед вызовом **LoadForm** по тому, что описано в разделе [Загрузка](loading-a-message-into-a-form.md)сообщения в форму . 
  

