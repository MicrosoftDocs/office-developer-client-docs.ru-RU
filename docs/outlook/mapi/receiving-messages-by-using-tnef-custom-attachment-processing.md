---
title: Получение сообщений с использованием настраиваемой обработки вложений TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Дата последнего изменения: 7 декабря 2015 года'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588029"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Получение сообщений с использованием настраиваемой обработки вложений TNEF

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы получать сообщения в формате TNEF с настроенной вложения обработки:
  
1. Импорт всех передаваемого свойств — те, которые поддерживает системы обмена сообщениями — из входящего сообщения в новое сообщение MAPI. Этот компонент включает текст сообщения, который содержит поток данных TNEF.
    
2. Определение и декодирования специальные вложения, содержащий поток TNEF.
    
3. Извлеките все вложения из входящего сообщения в MAPI вложений в новое сообщение MAPI. Восстановленную имена файлов, или других идентификационные маркеров на вложения, должны размещаться в свойство **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) нового вложения таким образом, метод [ITnef::ExtractProps](itnef-extractprops.md) позднее можно связать правильный вложения с тегами вложения, закодированный в качестве текста сообщения. 
    
4. Создание интерфейса OLE **IStream** обтекания декодированное поток TNEF и использовать этот объект, а также новые сообщения MAPI в вызове функции [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Вызовите метод **ITnef::ExtractProps** для восстановления из потока данных TNEF nontransmittable свойств в окне сообщения. 
    
6. Вызовите метод [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) с набором флаги MAPI_CREATE и MAPI_MODIFY. Этот вызов Удаляет теги вложения из текста сообщения и преобразует их в сведения о должности вложения в сообщение MAPI. 
    
7. Доставить сообщение через диспетчер очереди MAPI.
    

