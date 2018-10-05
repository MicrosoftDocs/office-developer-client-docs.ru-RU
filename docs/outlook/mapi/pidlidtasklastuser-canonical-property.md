---
title: Каноническое свойство PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390935"
---
# <a name="pidlidtasklastuser-canonical-property"></a>Каноническое свойство PidLidTaskLastUser

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Имя последнего пользователя, который был владелец задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskLastUser  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008122  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Перед клиента отправляет запрос задачи, это свойство присваивается имя назначено задач. Перед клиента отправляет Принятие задачи, это свойство присваивается имя исполнителя задачи. Перед клиента отправляет Отклонение задачи, это свойство присваивается имя назначено задач.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

