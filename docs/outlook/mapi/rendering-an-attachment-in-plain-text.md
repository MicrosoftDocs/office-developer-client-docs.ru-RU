---
title: Отрисовка вложения в виде обычного текста
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
# <a name="rendering-an-attachment-in-plain-text"></a>Отрисовка вложения в виде обычного текста

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы отрисовать вложение в сообщении с простым текстом, извлекаете свойство **PR_RENDERING_POSITION вложения** [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)и применяте его к данным в свойстве **PR_ATTACH_RENDERING** ([PidTagAttachRendering).](pidtagattachrendering-canonical-property.md) Существует два способа получения **PR_RENDERING_POSITION:**
  
- Откройте **вложение,** вызывая метод **IMessage::OpenAttach** сообщения, а затем запросив свойство PR_RENDERING_POSITION путем вызова метода **IMAPIProp::GetProps** вложения. Дополнительные сведения см. в подразделах [IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::GetProps.](imapiprop-getprops.md)
    
- Вызовите метод **IMessage::GetAttachmentTable** сообщения, чтобы получить доступ к таблице вложений и получить столбец, в PR_RENDERING_POSITION **свойства.** Этот способ всегда предпочтительный. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Помните, что многие хранилища сообщений с RTF не вычисляют PR_RENDERING_POSITION, пока клиент не запросит свойство **PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)сообщения.  До этого времени **PR_RENDERING_POSITION** обычно представляет приблизительное значение. Поставщики store сообщений могут предоставить клиентам приблизительное значение для повышения производительности. 
  
Отрисовка файла или двоичного вложения  хранится в PR_ATTACH_RENDERING свойстве. Вы можете получить PR_ATTACH_RENDERING так  же, как и **PR_RENDERING_POSITION:** непосредственно из вложения или из таблицы вложений. Для **PR_ATTACH_RENDERING** первая стратегия, хотя и более отнимает больше времени, является более безопасной. Так как некоторые поставщики хранимых сообщений утесируют столбцы таблицы до 255 или в некоторых  случаях — 510, сложно убедиться, что столбец PR_ATTACH_RENDERING содержит полную отрисовку. При искомом свойстве непосредственно из вложения оно всегда будет завершено. 
  
Ни OLE, ни вложения в сообщения не **PR_ATTACH_RENDERING.** Вместо этого данные отображения вложений OLE 1 хранятся в текстовом потоке сообщения. Вложения OLE 2 хранятся в специальном потоке объекта хранилища. Отрисовка сведений о вложениях сообщений доступна через диспетчер форм. 
  
 **Извлечение отображения вложения сообщения**
  
1. Используйте класс сообщения для доступа к диспетчеру форм.
    
2. Доступ к свойству PR_MINI_ICON **диспетчера** форм. Дополнительные сведения **см. в PR_MINI_ICON** ([PidTagMiniIcon).](pidtagminiicon-canonical-property.md)
    

