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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359266"
---
# <a name="pidtagmessageclass-canonical-property"></a>Каноническое свойство PidTagMessageClass

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит текстовую строку, идентифицирующую определяемый отправителем класс сообщений, например IPM.Note. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Идентификатор:  <br/> |0x001A  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Класс сообщения указывает тип сообщения. Он определяет набор свойств, определенных для сообщения, вид информации, которую передает сообщение, и обработку сообщения. 
  
Эти свойства содержат строки, совмещенные с периодами. Каждая строка представляет собой уровень подклассинга. Например, IPM. Примечание — это подкласс IPM и суперкласс IPM. Примечание.Private. 
  
Эти свойства должны состоять из символов ASCII от 32 до 127 и не должны закончиться периодом (ASCII 46). Сортировка и сравнение операций должны рассматриваться как строка, нечувствительная к делу. Максимальная возможная длина — 255 символов, но для того, чтобы позволить комнате MAPI использовать квалификаторы, рекомендуется сохранить исходную длину в 128 символов. 
  
Каждое сообщение необходимо предоставить эти свойства. Обычно клиентские приложения, создав новое сообщение, устанавливают его, как только [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) возвращается успешно. Но если свойство не установлено, когда клиент вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)магазин сообщений должен установить его на IPM. 
  
Значения, определенные MAPI: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM и IPC предназначены только для суперклассов, и перед хранением или отправкой сообщение должно иметь по крайней мере один квалификатор подкласса. Дополнительные сведения об использовании класса сообщений см. в [сообщении Классов.](mapi-message-classes.md) Списки необходимых и необязательных свойств для классов сообщений см. в подтопику [о свойствах сообщений.](message-properties-overview.md)
  
Настраиваемый класс сообщений может определять свойства в зарезервированном диапазоне только для этого класса сообщений. Дополнительные сведения см. [в дополнительных сведениях о идентификаторах свойств.](mapi-property-identifier-overview.md) 
  
Управление классами сообщений, в которых хранится папка входящих сообщений. Дополнительные сведения см. в [методе IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) 
  
Дополнительные сведения об использовании классов сообщений с формами и серверами форм см. в [подборе класса сообщений.](choosing-a-message-class.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для представления голосовой почты и факсимили.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

