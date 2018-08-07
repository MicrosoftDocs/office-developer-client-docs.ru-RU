---
title: Блок данных ИзменитьЗапись (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Чтобы изменить значения, содержащиеся в существующей записи можно использовать блок данных ИзменитьЗапись.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806942"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Блок данных ИзменитьЗапись (приложение настраиваемых web Access)

Чтобы изменить значения, содержащиеся в существующей записи можно использовать блок данных **ИзменитьЗапись** . 
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Блок данных **ИзменитьЗапись** доступна только в макросов данных. 
  
## <a name="setting"></a>Параметр

Блок данных **ИзменитьЗапись** имеет следующие аргументы. 
  
|**Argument**|**Описание**|
|:-----|:-----|
|**Alias** <br/> |Строка, идентифицирующая записи для редактирования. Если аргумент *псевдоним* не задан, изменяется текущей записи.  <br/> |
   
## <a name="remarks"></a>Замечания

После оператора **ИзменитьЗапись** можно вставить блок команды, которые будут выполняться до подтверждения изменений в запись. В блока данных **ИзменитьЗапись** доступны следующие действия. 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Затем... Оператор Else макросов](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Действие **SetField** используется для указания нового значения поля в измененной записи. 
  
**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия. 
  
Чтобы отменить редактирование записи, используйте действие **CancelRecordChange** . Это предотвращает фиксации изменений и выполняет выход из блока данных **ИзменитьЗапись** . 
  
Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** . Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


