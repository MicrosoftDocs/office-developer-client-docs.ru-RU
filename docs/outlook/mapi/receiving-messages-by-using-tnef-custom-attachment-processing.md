---
title: Получение сообщений с помощью настраиваемой обработки вложений в TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429322"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Получение сообщений с помощью настраиваемой обработки вложений в TNEF

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы получить сообщение tNEF с настраиваемой обработкой вложений:
  
1. Импорт всех передаваемых свойств (поддерживаемых системой обмена сообщениями) из входящих сообщений в новое сообщение MAPI. К ним относится текст сообщения, который содержит поток данных TNEF.
    
2. Определите и расшифруйте специальное вложение, которое содержит поток TNEF.
    
3. Извлекать все вложения из входящих сообщений во вложения MAPI в новом сообщении MAPI. Восстановленные имена файлов или другие идентифицирующие маркеры во вложениях следует поместить в свойство **PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName)](pidtagattachtransportname-canonical-property.md)новых вложений, чтобы метод [ITnef::ExtractProps](itnef-extractprops.md) позднее может связать правильное вложение с тегами вложений, закодированных в тексте сообщения. 
    
4. Создайте интерфейс OLE **IStream** для обтекаия декодирования потока TNEF и используйте этот объект вместе с новым сообщением MAPI в вызове функции [OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Вызовите метод **ITnef::ExtractProps,** чтобы восстановить несмещенные свойства сообщения из потока данных TNEF. 
    
6. Вызовите [метод ITnef::OpenTaggedBody](itnef-opentaggedbody.md) с установленными MAPI_CREATE и MAPI_MODIFY флагами. Этот вызов удаляет теги вложений из текста сообщения и преобразует их в сведения о положении вложения в сообщении MAPI. 
    
7. Доставка сообщения через пульер MAPI.
    

