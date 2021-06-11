---
title: Получение сообщений с помощью пользовательской обработки вложений TNEF
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
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Получение сообщений с помощью пользовательской обработки вложений TNEF

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получение сообщения TNEF с настраиваемой обработкой вложений:
  
1. Импортировать все передаваемые свойства — те, которые поддерживает система обмена сообщениями — из входящих сообщений в новое сообщение MAPI. Это включает текст сообщения, содержащий поток данных TNEF.
    
2. Определите и расшифруйте специальное вложение, содержаное поток TNEF.
    
3. Извлекать все вложения из входящих сообщений в вложения MAPI в новом сообщении MAPI. Восстановленные имена файлов или другие маркеры идентификации на вложениях должны быть помещены в **свойство PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName)](pidtagattachtransportname-canonical-property.md)новых вложений, чтобы метод [ITnef::ExtractProps](itnef-extractprops.md) позже связывал правильное вложение с тегами вложений, закодированных в тексте сообщения. 
    
4. Создайте интерфейс OLE **IStream** для обмотки расшифровки потока TNEF и используйте этот объект вместе с новым сообщением MAPI в вызове функции [OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Вызов метода **ITnef::ExtractProps** для восстановления нетрансмитируемых свойств сообщения из потока данных TNEF. 
    
6. Вызов метода [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) с набором MAPI_CREATE и MAPI_MODIFY флагов. Этот вызов удаляет теги вложений из текста сообщения и преобразует их в сведения о положении вложений в сообщении MAPI. 
    
7. Доставка сообщения через шпалер MAPI.
    

