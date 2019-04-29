---
title: Блок данных ИзменитьЗапись (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Вы можете использовать блок данных ИзменитьЗапись, чтобы изменить значения, хранящиеся в существующей записи.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418346"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Блок данных ИзменитьЗапись (пользовательское веб-приложение для Access)

Вы можете использовать блок данных **ИзменитьЗапись** , чтобы изменить значения, хранящиеся в существующей записи. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Блок данных **ИзменитьЗапись** доступен только в макросах данных. 
  
## <a name="setting"></a>Setting

Блок данных **ИзменитьЗапись** имеет следующие аргументы. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|**Alias** <br/> |Строка, определяющая изменяемую запись. Если аргумент *Alias* не указан, текущая запись редактируется.  <br/> |
   
## <a name="remarks"></a>Примечания

После оператора **ИзменитьЗапись** вы можете вставить блок команд, который будет выполняться перед фиксацией изменений записи. Следующие действия доступны в блоке данных **ИзменитьЗапись** . 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Then... Оператор else макроса](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Используйте действие **SetField** для указания новых значений поля в измененной записи. 
  
Можно использовать выражение **If... Then... Else** для выполнения операций на основе условия. 
  
Чтобы отменить редактирование записи, используйте действие **канцелрекордчанже** . Это предотвращает фиксацию изменений и выход из блока данных **ИзменитьЗапись** . 
  
Локальную переменную **ласткреатерекордидентити** можно использовать для работы с последней записью, созданной в блоке данных **СоздатьЗапись** . Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


