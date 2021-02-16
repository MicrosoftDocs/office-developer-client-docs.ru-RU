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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит текстовую строку, идентифицирующую определяемый отправителем класс сообщений, например IPM.Note. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Идентификатор:  <br/> |0x001A  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Класс сообщения указывает тип сообщения. Он определяет набор свойств, определенных для сообщения, тип передаемой в сообщении информации и обработку сообщения. 
  
Эти свойства содержат строки, совмещенные с точкими. Каждая строка представляет уровень подклассов. Например, IPM. Примечание. Это подкласс IPM и суперкласс IPM. Note.Private. 
  
Эти свойства должны состоять из символов ASCII от 32 до 127 и не должны заканчиваются точками (ASCII 46). Операции сортировки и сравнения должны рассматриваться как строка без сноски. Максимальная возможная длина — 255 символов, но чтобы разрешить квалификаторы MAPI, рекомендуется сохранить исходную длину до 128 символов. 
  
Каждое сообщение необходимо предоставить эти свойства. Обычно клиентские приложения, создав новое сообщение, устанавливают его, как только [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) возвращается успешно. Но если свойство не было установлено, когда клиент вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)хранилище сообщений должно установить для него IPM. 
  
MapI определяет значения: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM и IPC предназначены только для использования в качестве суперклассов, а перед хранением или отправкой сообщения должен быть по крайней мере один квалификатор подкласса. Дополнительные сведения об использовании класса сообщений см. [в сведениях о классах сообщений.](mapi-message-classes.md) Список необходимых и необязательных свойств для классов сообщений см. в подзаголовках ["Свойства сообщения".](message-properties-overview.md)
  
Настраиваемый класс сообщений может определять свойства в зарезервированном диапазоне для использования только с этим классом сообщений. Дополнительные сведения см. [в документе "Идентификаторы свойств".](mapi-property-identifier-overview.md) 
  
Классы сообщений контролируют, в какой папке будет храниться входящие сообщения. Дополнительные сведения см. в [методе IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) 
  
Дополнительные сведения об использовании классов сообщений с формами и серверами форм см. в подклассе ["Выбор класса сообщений".](choosing-a-message-class.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для представления голосовой почты и факсимили.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

