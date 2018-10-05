---
title: Каноническое свойство PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396668"
---
# <a name="pidtagmessageclass-canonical-property"></a>Каноническое свойство PidTagMessageClass

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит текстовую строку, которая определяет класс отправителя определенное сообщение, такие как IPM. Примечание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Идентификатор:  <br/> |0x001A  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Замечания

Класс сообщения указывает тип сообщения. Определяет набор свойств, определенных в сообщении передает сведения сообщения и как обрабатывать сообщения. 
  
Эти свойства содержат строк, объединяется с периодов. Каждая строка представляет уровень подклассы. Например IPM. Примечание это подкласс IPM и суперклассом IPM. Note.Private. 
  
Эти свойства должны состоять из знаков ASCII 32 до 127 и не должно заканчиваться точкой (ASCII 46). Сортировка и сравнение операций должен обрабатывать его как строка без учета регистра. Возможные Максимальная длина составляет 255 символов, но чтобы разрешить места MAPI для добавления классификаторы рекомендуется что исходное значение длины должны сохраняться в разделе 128 символов. 
  
Каждому сообщению требуется бесплатной этих свойств. Как правило клиентское приложение, создавать новые сообщения устанавливает его сразу после [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) пройдет успешно. Однако если свойство не задано, когда клиент вызывает [IMAPIProp::SaveChanges](imapiprop-savechanges.md), хранилища сообщений следует присвоить IPM. 
  
Поддерживаются следующие значения, определенные в MAPI: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM и производственных Издержек предназначенного для формирования только суперклассов и сообщения должен иметь по крайней мере один квалификатор подкласс добавляться перед хранимых или отправки. Дополнительные сведения об использовании класс сообщения можно [Классов сообщений](mapi-message-classes.md). Списки необходимые и дополнительные свойства для классов сообщений содержатся в разделе [о](message-properties-overview.md)свойств сообщения.
  
Пользовательский класс сообщения можно определить свойства в диапазоне зарезервировано для использования с только что класс сообщения. Дополнительные сведения [Об идентификаторах свойств](mapi-property-identifier-overview.md)см. 
  
Классы сообщений элемента управления, который получать папку входящих сообщений хранится в. Для получения дополнительных сведений см [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Дополнительные сведения об использовании классов сообщений с помощью форм и форм серверы [Класс сообщения](choosing-a-message-class.md)см. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для представления сообщений голосовой почты и факсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

