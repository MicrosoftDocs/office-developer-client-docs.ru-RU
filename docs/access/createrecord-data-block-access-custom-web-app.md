---
title: CreateRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Для создания новой записи в указанной таблице можно использовать блок данных CreateRecord.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421377"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>CreateRecord Data Block (Access custom web app)

Для создания новой записи в указанной таблице можно использовать блок данных **CreateRecord.** 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Блок **данных CreateRecord** доступен только в макросах данных. 
  
## <a name="setting"></a>Setting

Блок **данных CreateRecord** имеет следующие аргументы. 
  
Блок **данных CreateRecord** имеет следующие аргументы. 
  
|**Имя аргумента**|**Обязательный**|**Описание**|
|:-----|:-----|:-----|
|**Создание записи** <br/> |Да  <br/> |Имя таблицы для создания новой записи.  <br/> |
|**Alias** <br/> |Нет  <br/> |Строка, идентифицирует запись. Вы можете использовать псевдоним записи для идентификации  <br/> |
   
## <a name="remarks"></a>Примечания

Запись, созданная **CreateRecord,** автоматически становится текущей. 
  
После **заявления CreateRecord** можно вставить блок команд, которые будут выполняться до выполнения новой записи. Следующие действия доступны в блоке **данных CreateRecord.** 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[Если... Затем... Else Macro Statement](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
После создания записи действие **CreateRecord** используйте действие **SetField** для указания значения поля в новой записи. 
  
Вы можете использовать **if... Затем... Другое** заявление для выполнения операций на основе условия. 
  
Чтобы отменить создание записи, используйте **действие CancelRecordChange.** Это предотвращает совершение изменений и выход из **блока данных CreateRecord.** 
  
После совершения новой записи можно использовать локализованную переменную **LastCreateRecordIdentity** для работы с записью. Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


