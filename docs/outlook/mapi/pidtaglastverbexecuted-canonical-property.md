---
title: Каноническое свойство PidTagLastVerbExecuted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9abd4eb955428595ebe41ab9b2c661303ee2779a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279617"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>Каноническое свойство PidTagLastVerbExecuted

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит последний выполненный глагол.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|Идентификатор:  <br/> |0x1081  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |History  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь одно из следующих значений:
  
|**Verb**|**Значение свойства**|
|:-----|:-----|
|Запись  <br/> |0x00000001  <br/> |
|Другое  <br/> |0x00000003  <br/> |
|Чтение почты  <br/> |0x00000100  <br/> |
|Нечитаемая почта  <br/> |0x00000101  <br/> |
|Отправленная почта  <br/> |0x00000102  <br/> |
|Неавентная почта  <br/> |0x00000103  <br/> |
|Почта получения  <br/> |0x00000104  <br/> |
|Ответная почта  <br/> |0x00000105  <br/> |
|Пересылаемая почта  <br/> |0x00000106  <br/> |
|Удаленная почта  <br/> |0x00000107  <br/> |
|Получение доставки  <br/> |0x00000108  <br/> |
|Получение чтения  <br/> |0x00000109  <br/> |
|Квитанция о неделиверии  <br/> |0x0000010A  <br/> |
|Нечитаемая квитанция  <br/> |0x0000010B  <br/> |
|Recall_S почты  <br/> |0x0000010C  <br/> |
|Recall_F почты  <br/> |0x0000010D  <br/> |
|Отслеживание почты  <br/> |0x0000010E  <br/> |
|Не Office почты  <br/> |0x0000011B  <br/> |
|Отзыв почты  <br/> |0x0000011C  <br/> |
|Отслеживаемая почта  <br/> |0x00000139  <br/> |
|Contact  <br/> |0x00000200  <br/> |
|Список рассылки  <br/> |0x00000201  <br/> |
|Липкий примечание, синий  <br/> |0x00000300  <br/> |
|Липкий Примечание, Зеленый  <br/> |0x00000301  <br/> |
|Липкий примечание, Розовый  <br/> |0x00000302  <br/> |
|Липкий примечание, желтый  <br/> |0x00000303  <br/> |
|Липкий Примечание, Белый  <br/> |0x00000304  <br/> |
|Назначение одного экземпляра  <br/> |0x00000400  <br/> |
|Повторяющиеся встречи  <br/> |0x00000401  <br/> |
|Собрание одного экземпляра  <br/> |0x00000402  <br/> |
|Повторяющиеся собрания  <br/> |0x00000403  <br/> |
|Запрос на собрание / полное обновление  <br/> |0x00000404  <br/> |
|Accept  <br/> |0x00000405  <br/> |
|Отклонение  <br/> |0x00000406  <br/> |
|Предварительно принять  <br/> |0x00000407  <br/> |
|Отмена  <br/> |0x00000408  <br/> |
|Информационное обновление  <br/> |0x00000409  <br/> |
|Обновление задачи и задачи  <br/> |0x00000500  <br/> |
|Не назначенная повторяемая задача  <br/> |0x00000501  <br/> |
|Задача ассимилита  <br/> |0x00000502  <br/> |
|Задача назначитель  <br/> |0x00000503  <br/> |
|Запрос задачи  <br/> |0x00000504  <br/> |
|Принятие задач  <br/> |0x00000505  <br/> |
|Отклонение задачи  <br/> |0x00000506  <br/> |
|Беседа журнала  <br/> |0x00000601  <br/> |
|Сообщение электронной почты журнала  <br/> |0x00000602  <br/> |
|Запрос на собрание журнала  <br/> |0x00000603  <br/> |
|Ответ на собрание журнала  <br/> |0x00000604  <br/> |
|Запрос задачи журнала  <br/> |0x00000606  <br/> |
|Ответ задачи журнала  <br/> |0x00000607  <br/> |
|Примечание журнала  <br/> |0x00000608  <br/> |
|Факс журнала  <br/> |0x00000609  <br/> |
|Вызов Телефон журнала  <br/> |0x0000060A  <br/> |
|Задача журнала  <br/> |0x0000060B  <br/> |
|Письмо журнала  <br/> |0x0000060C  <br/> |
|Журнал Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Журнал Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Журнал Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Доступ Microsoft Office журнала  <br/> |0x00000610  <br/> |
|Документ журнала  <br/> |0x00000612  <br/> |
|Собрание журнала  <br/> |0x00000613  <br/> |
|Отмена собрания журнала  <br/> |0x00000614  <br/> |
|Удаленный сеанс журнала  <br/> |0x00000615  <br/> |
|Новая почта  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

