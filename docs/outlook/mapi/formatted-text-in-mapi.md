---
title: Форматированный текст в MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 6b82a755cbf2c8bd0f1d3676d4560e131dce3bd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808495"
---
# <a name="formatted-text-in-mapi"></a>Форматированный текст в MAPI

  
  
**Применимо к**: Outlook 
  
Текст сообщения, можно хранить и передаваемые сведения с помощью обычного текста или форматированный текст. Форматированный текст путем изменения внешнего вида в организации, например, один или несколько шрифтов, размеры шрифтов или цвета текста улучшает текста сообщения. Рекомендуется все клиенты и по возможности все поставщики хранилища сообщений, поддерживают форматированный текст. Поддержка форматированный текст в сообщениях добавляется значение, улучшение читаемости сообщения и внеся обработки сообщений и удобнее.
  
Форматированный текст можно реализовать в различными способами. Чаще всего используется с форматированный текст (RTF). MAPI определяет три передаваемого свойства для хранения сведений текст сообщения: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для обычного текста, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) для HTML и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) для текст RTF, которая была свернута. Так как версию форматированный текст сообщения может быть дважды мере версия без форматирования, текст RTF сжимается до перемещать его с сообщением и хранится в свойстве **PR_RTF_COMPRESSED** . После отображения сообщения на экране несжатую с помощью служебной программы функции, предоставляемые MAPI. 
  
MAPI определяет эти два свойства: текстовое сообщение и механизмы для преобразования между ними, чтобы принять во внимание RTF клиенты могут взаимодействовать с клиентами и систем обмена сообщениями, которые не поддерживают форматированный текст.
  
### 

[Синхронизация текста и форматирования](synchronizing-text-and-formatting.md)
  
> Описывается, как синхронизировать с форматированием текст сообщения RTF.
    
[Поддержка форматированный текст в исходящих сообщений: обязанности клиента](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Описывает обязанности клиентского приложения для поддержки форматированный текст в исходящих сообщений.
    
[Поддержка форматированный текст в входящих сообщений: обязанности клиента](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Описывает обязанности клиентского приложения для поддержки форматированный текст в входящих сообщений.
    
[Поддержка форматированный текст: Обязанности хранилища сообщений](supporting-formatted-text-message-store-responsibilities.md)
  
> Описывает обязанности хранилища сообщений для поддержки форматированный текст.
    
[Поддержка форматированный текст: Отображение вложений](supporting-formatted-text-rendering-attachments.md)
  
> Описывает способ выбора, где отображаются вложения.
    
[Поддержка форматированный текст: Обязанности шлюза](supporting-formatted-text-gateway-responsibilities.md)
  
> Описывает обязанности шлюза для входящих и исходящих сообщений форматированный текст.
    
