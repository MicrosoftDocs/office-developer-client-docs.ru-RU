---
title: CreateRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Блок данных CreateRecord можно использовать для создания новой записи в указанной таблице.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421377"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>CreateRecord Data Block (Access custom web app)

Блок данных **CreateRecord можно использовать** для создания новой записи в указанной таблице. 
  
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
|**Alias** <br/> |Нет  <br/> |Строка, идентифицирует запись. Псевдоним записи можно использовать для идентификации  <br/> |
   
## <a name="remarks"></a>Примечания

Запись, созданная **с помощью CreateRecord,** автоматически становится текущей записью. 
  
После **записи CreateRecord** можно вставить блок команд, которые будут выполняться до того, как будет зафиксирована новая запись. В блоке данных **CreateRecord** доступны следующие действия. 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Затем... Else Macro Statement](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
После создания записи с помощью действия **CreateRecord** используйте действие **SetField,** чтобы указать значение поля в новой записи. 
  
Вы можете использовать **if... Затем... Заявление Else** для выполнения операций на основе условия. 
  
Чтобы отменить создание записи, используйте действие **CancelRecordChange.** Это предотвращает зафиксирование изменений и выход из блока **данных CreateRecord.** 
  
После записи можно использовать локализованную переменную **LastCreateRecordIdentity** для работы с записью. Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


