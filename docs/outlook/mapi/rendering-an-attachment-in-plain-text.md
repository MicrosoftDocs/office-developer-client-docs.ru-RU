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
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410877"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Отображение вложения в виде обычного текста

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы отобразить вложение в сообщении с обычным текстом, извлеките свойство **PR_RENDERING_POSITION** вложения ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) и примените его к данным в свойстве **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)). Получить **PR_RENDERING_POSITION**можно двумя способами:
  
- Откройте вложение, вызвав метод Message **iMessage:: опенаттач** и запросите свойство **PR_RENDERING_POSITION** , вызвав метод вложения **IMAPIProp::** . Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md) and [IMAPIProp:: PROPS](imapiprop-getprops.md).
    
- Вызовите метод **iMessage:: жетаттачменттабле** , чтобы получить доступ к своей таблице вложений, и извлеките столбец, содержащий свойство **PR_RENDERING_POSITION** . Таким образом, всегда предпочтительнее. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Имейте в виду, что многие хранилища сообщений с поддержкой RTF не рассчитывают **PR_RENDERING_POSITION** до тех пор, пока клиент не запросит свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) сообщения. До наступления этого времени **PR_RENDERING_POSITION** обычно представляет приблизительное значение. Поставщики хранилищ сообщений могут предоставлять клиентам приблизительные значения для улучшения производительности. 
  
Отрисовка для файла или двоичного вложения хранится в свойстве **PR_ATTACH_RENDERING** . Вы можете выбрать получение **PR_ATTACH_RENDERING** с теми же способами, что и при получении **PR_RENDERING_POSITION**: непосредственно из вложения или из таблицы вложений. Для **PR_ATTACH_RENDERING**Первая стратегия, хотя и более длительное время, более безопасна. Так как некоторые поставщики хранилищ сообщений усекаются столбцы таблицы до 255 байт, или в нескольких случаях 510 байт, трудно убедиться в том, что столбец **PR_ATTACH_RENDERING** содержит полную визуализацию. При получении свойства непосредственно из вложения он всегда будет полным. 
  
**PR_ATTACH_RENDERING**не задаются ни вложениями OLE, ни вложениями сообщений. Вместо этого сведения о отрисовке для вложений OLE 1 хранятся в потоке текста сообщения. Для вложений OLE 2 оно хранится в специальном дочернем потоке объекта Storage. Отображение сведений о вложениях сообщений осуществляется с помощью диспетчера форм. 
  
 **Получение отображения вложения сообщения**
  
1. Используйте класс сообщения для доступа к диспетчеру форм.
    
2. Доступ к свойству **PR_MINI_ICON** диспетчера форм. Дополнительные сведения см **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

