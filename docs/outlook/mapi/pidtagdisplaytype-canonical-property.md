---
title: Каноническое свойство PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360783"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Каноническое свойство PidTagDisplayType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, используемое для связи значка с определенной строкой таблицы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Идентификатор:  <br/> |0x3900  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит длинное целое число, которое упрощает специальную обработку записи в таблице на основе ее типа. Эта специальная обработка обычно состоит из отображения значка или другого элемента отображения, связанного с типом отображения. 
  
Это свойство не используется в таблицах содержимого папок. Клиентские приложения должны использовать свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения и соответствующий интерфейс [имапиформинфо](imapiforminfoimapiprop.md) , чтобы получить свойства **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) и **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) для этого сообщения. 
  
Это свойство может иметь только одно из следующих значений:
  
DT_AGENT 
  
> Автоматический агент, например, отображение квоты или диаграммы погоды.
    
DT_DISTLIST 
  
> Список рассылки.
    
DT_FOLDER 
  
> Отображение значка папки по умолчанию рядом с папкой.
    
DT_FOLDER_LINK 
  
> Отображать значок ссылки на папку по умолчанию рядом с папкой, а не значком папки по умолчанию.
    
DT_FOLDER_SPECIAL 
  
> Значок для папки с различием, характерным для приложения, например специальным типом общедоступной папки.
    
DT_FORUM 
  
> Форум, например служба доски объявлений или общедоступная или общая папка.
    
DT_GLOBAL 
  
> Глобальная адресная книга.
    
DT_LOCAL 
  
> Локальная адресная книга, к которой вы предоставляете доступ из небольшой рабочей группы.
    
DT_MAILUSER 
  
> Типичный пользователь обмена сообщениями.
    
DT_MODIFIABLE 
  
> Допуска контейнер должен быть отмечен как изменяемый в пользовательском интерфейсе.
    
DT_NOT_SPECIFIC 
  
> Не совпадают с другими параметрами.
    
DT_ORGANIZATION 
  
> Специальный псевдоним, определенный для большой группы, например служба технической поддержки, учетная запись или координатор крови.
    
DT_PRIVATE_DISTLIST 
  
> Частный административный список рассылки.
    
DT_REMOTE_MAILUSER 
  
> Получатель, который известен из внешней или удаленной системы обмена сообщениями.
    
DT_WAN 
  
> Адресная книга глобальной сети.
    
В таблицах содержимого адресных книг используются значения DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST и DT_REMOTE_MAILUSER. В таблицах иерархии адресных книг и в одноразовых таблицах используются значения DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC и DT_WAN. В таблицах иерархии папок используются значения DT_FOLDER, DT_FOLDER_LINK и DT_FOLDER_SPECIAL. 
  
Если это свойство не задано, клиент должен предполагать тип по умолчанию, который подходит для таблицы, обычно DT_FOLDER, DT_LOCAL или DT_MAILUSER. 
  
 **Note (Примечание** ) Все значения, которые не задокументированы, зарезервированы для MAPI. Клиентские приложения не должны определять новые значения и должны быть готовы к работе с недокументированным значением. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для шаблонов адресных книг.
    
[[MS — ОКСЛДАП]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Включает доступ к каталогу.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

