---
title: Блок данных СоздатьЗапись (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Блок данных СоздатьЗапись можно использовать для создания новой записи в указанную таблицу.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806987"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>Блок данных СоздатьЗапись (приложение настраиваемых web Access)

Блок данных **СоздатьЗапись** можно использовать для создания новой записи в указанную таблицу. 
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Блок данных **СоздатьЗапись** доступна только в макросов данных. 
  
## <a name="setting"></a>Параметр

Блок данных **СоздатьЗапись** имеет следующие аргументы. 
  
Блок данных **СоздатьЗапись** имеет следующие аргументы. 
  
|**Имя аргумента**|**Обязательное**|**Описание**|
|:-----|:-----|:-----|
|**Создание записи в** <br/> |Да  <br/> |Имя таблицы для создания новой записи в.  <br/> |
|**Alias** <br/> |Нет  <br/> |Строка, идентифицирующая эту запись. Можно использовать эту запись псевдонима для идентификации  <br/> |
   
## <a name="remarks"></a>Замечания

Записи, созданной **СоздатьЗапись** автоматически становится текущей. 
  
После оператора **СоздатьЗапись** можно вставить блок команды, которые будут выполняться перед сохранением новую запись. В блоке данных **СоздатьЗапись** доступны следующие действия. 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Затем... Оператор Else макросов](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
После **СоздатьЗапись** действие создает запись, используйте действие **SetField** для указания значения поля в новую запись. 
  
**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия. 
  
Чтобы отменить создание записи, используйте действие **CancelRecordChange** . Это предотвращает фиксации изменений и выполняет выход из блока **СоздатьЗапись** данных. 
  
После фиксации новую запись локальной переменной **LastCreateRecordIdentity** можно использовать для работы с записью. Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


