---
title: Отображение вложения в виде обычного текста
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 38db1d18f240188c7566a57afa23291a307446dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812135"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Отображение вложения в виде обычного текста

  
  
**Относится к**: Outlook 
  
Для отображения вложения в сообщение с помощью обычного текста, получения вложений свойство **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) и его применения к данным в **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) свойство. Для получения **PR_RENDERING_POSITION**двумя способами:
  
- Открывать вложения, вызвав метод **IMessage::OpenAttach** сообщений и затем задайте для свойства **PR_RENDERING_POSITION** путем вызова метода **IMAPIProp::GetProps** вложения. Для получения дополнительных сведений см [IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Вызовите метод **IMessage::GetAttachmentTable** сообщений для доступа к его таблицы вложений и получить столбец, в котором содержатся свойства **PR_RENDERING_POSITION** . В этом случае всегда является предпочтительным. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Имейте в виду, многие принять во внимание RTF хранилищ сообщений не вычисление **PR_RENDERING_POSITION** , пока клиент запрашивает свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) сообщения. До этого времени **PR_RENDERING_POSITION** обычно представляет приблизительное значение. Поставщики хранилища сообщений могут предоставить клиентам с приблизительное число для улучшения производительности. 
  
Отображение для файла или двоичные вложения хранится в своем свойстве **PR_ATTACH_RENDERING** . У вас есть выбор извлечение **PR_ATTACH_RENDERING** же образом, как получить **PR_RENDERING_POSITION**: непосредственно из вложения или из таблицы вложений. Для **PR_ATTACH_RENDERING**, первый стратегия хотя занимает больше времени, является более безопасным. Так как некоторые поставщики хранилища сообщений усекать их столбцов таблицы до 255 байт или в некоторых случаях 510 байт, трудно убедитесь, что столбец **PR_ATTACH_RENDERING** содержит полный визуализации. При получении свойства непосредственно из вложения, он всегда будет завершен. 
  
Вложения сообщения ни OLE задайте **PR_ATTACH_RENDERING**. Вместо этого сведения о визуализации для вложения OLE 1 хранятся в потоке текста сообщения. Для вложения OLE 2 он хранится в поток специальные дочернего объекта хранилища. Отображение сведений для вложений сообщений доступен через диспетчер форм. 
  
 **Для получения визуализации для вложения сообщения**
  
1. Используйте класс сообщения сообщения для доступа к диспетчеру формы.
    
2. Доступ к свойству **PR_MINI_ICON** диспетчер форм. Для получения дополнительных сведений см **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

