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
# <a name="composing-a-new-message-by-using-a-form"></a>Составление нового сообщения с помощью формы

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы использовать форму для создания нового сообщения, сначала необходимо создайте новый объект настраиваемого сообщения.
  
 **Чтобы создать новое сообщение с помощью формы**
  
1. Вызовите метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) диспетчер форм, чтобы получить указатель на объект данных формы — это объект, реализующий [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) интерфейса. 
    
2. Передайте указатель мыши в объект данных формы в вызове [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** загружает server соответствующую форму. Кроме того передайте идентификатор интерфейса **CreateForm** для указания интерфейса, которые будут использоваться для доступа к нового сообщения. Как правило, запрос [IPersistMessage: IUnknown](ipersistmessageiunknown.md) , передав IID_IPersistMessage **CreateForm**.
    
3. Сохраните новые сообщения путем вызова метода [IPersistMessage::Save](ipersistmessage-save.md) . Сервера форм следует задать значения для свойства необходимые сообщения при создании сообщения. 
    
4. Загружать сообщения с помощью одного из двух стратегий: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) или [IMAPISession::PrepareForm](imapisession-prepareform.md) следуют [IMAPISession::ShowForm](imapisession-showform.md). Дополнительные сведения об этих стратегий см [В форме сообщения](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Существует возможности для повышения производительности при загрузке нового настраиваемого сообщения в форме сервера, так как возможность получить сведения о сообщении уже были применены, такие как его класса сообщений — во время обработки, необходимые для ** ResolveMessageClass** и вызывает метод **CreateForm** . Таким образом вы сможете упростить обработки, требуемые до вызова **LoadForm** через, как описано в разделе [Загрузка в форме сообщения](loading-a-message-into-a-form.md). 
  

