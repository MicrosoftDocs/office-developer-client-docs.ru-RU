---
title: Отрисовка вложения в простом тексте
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410877"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Отрисовка вложения в простом тексте

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы отрисовать вложение в сообщении с простым **текстом, извлекаем** свойство [PR_RENDERING_POSITION (PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)и применяем его к данным в **свойстве** [PR_ATTACH_RENDERING (PidTagAttachRendering).](pidtagattachrendering-canonical-property.md) Существует два способа получения **PR_RENDERING_POSITION:**
  
- Откройте **вложение,** назвав метод **IMessage::OpenAttach,** а затем попросите свойство PR_RENDERING_POSITION, назвав метод **IMAPIProp::GetProps** вложения. Дополнительные сведения см. [в странице IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Вызовите метод **IMessage::GetAttachmentTable,** чтобы получить доступ к таблице вложений и получить столбец, который содержит **свойство** PR_RENDERING_POSITION. Этот способ всегда предпочтительнее. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Имейте в виду, что многие хранилища сообщений, PR_RENDERING_POSITION RTF, не  вычисляют PR_BODY[(PidTagBody)](pidtagbody-canonical-property.md)свойства сообщения.  До этого времени **PR_RENDERING_POSITION** обычно представляет приблизительное значение. Поставщикам магазинов сообщений разрешено поставлять клиентам приблизительное значение для повышения производительности. 
  
Отрисовка для файла или двоичного вложения хранится в **PR_ATTACH_RENDERING** свойстве. Вы можете извлекать PR_ATTACH_RENDERING  так же, как и **PR_RENDERING_POSITION:** непосредственно из вложения или из таблицы вложений. Для **PR_ATTACH_RENDERING** первая стратегия, хотя и отнимает больше времени, является более безопасной. Так как некоторые поставщики магазинов сообщений усечены столбцы таблицы до 255 bytes или в нескольких  случаях 510 bytes, трудно быть уверенным, что столбец PR_ATTACH_RENDERING содержит полное отрисовку. При ирисовыве свойства непосредственно из вложения оно всегда будет завершено. 
  
Ни OLE, ни вложения сообщений **не PR_ATTACH_RENDERING**. Вместо этого в текстовом потоке сообщения сохраняется отрисовка сведений для вложений OLE 1. Для вложений OLE 2 он хранится в специальном детском потоке объекта хранения. Отрисовка сведений для вложений сообщений доступна через диспетчер форм. 
  
 **Извлечение отрисовки для вложения сообщений**
  
1. Чтобы получить доступ к диспетчеру форм, используйте класс сообщения сообщения.
    
2. Доступ к свойству администратора **PR_MINI_ICON** формы. Дополнительные сведения см. **в PR_MINI_ICON** [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md)
    

