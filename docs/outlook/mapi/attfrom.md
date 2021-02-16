---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432417"
---
# <a name="attfrom"></a>attFrom

**Относится к**: Outlook 2013 | Outlook 2016 
  
Атрибут **attFrom** закодирован как структура **TRP,** которая кодирует отображаемую и адрес электронной почты отправитель, а затем отображаемую и адрес отправитель, а затем все необходимые заполнения. Формат **attFrom:** 
  
**attFrom**: _sender-display-name_ _sender-address _padding в структуре TRP 
    
The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary. Заполнение в конце кодиру **attFrom** состоит из максимального объема символов null, необходимого для достижения границы **sizeof(TRP).** 
  
_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb 
    
Для **элемента attFrom** структура **TRP** всегда является однофазной кодирой, поэтому в качестве trpid от поля структуры **TRP** всегда является **trpidOneOff.** Элементы cbgrtrp, cch и cb соответствуют оставшимся полям структуры **TRP.** 
  
Поле cbgrtrp вычисляется как сумма **(sizeof(TRP) \* 2),** длина нулевого имени sender-display-name с его заполнением и длина завершаемого null адреса отправитель.
  
Поле cch вычисляется как длина отображаемого имени, о завершаемого null, с его заполнением.
  
Поле cb вычисляется как длина завершаемого null-адреса отправитель.
  
_sender-address:_ address-type **:** address **'\0'**
    
Адрес отправитель — это строка, состоящая из четырех частей: типа адреса, литерального двоеточия (:), самого адреса и завершающих символов null. Например, строка `fax:1-909-555-1234\0` будет иметь юридическое значение адреса отправитель.
  

