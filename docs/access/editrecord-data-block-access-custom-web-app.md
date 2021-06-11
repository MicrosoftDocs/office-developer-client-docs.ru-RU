---
title: Блок данных EditRecord (Доступ к пользовательскому веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Блок данных EditRecord можно использовать для изменения значений, содержащихся в существующей записи.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418346"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Блок данных EditRecord (Доступ к пользовательскому веб-приложению)

Блок данных **EditRecord можно** использовать для изменения значений, содержащихся в существующей записи. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Блок **данных EditRecord** доступен только в макросах данных. 
  
## <a name="setting"></a>Setting

Блок **данных EditRecord** имеет следующие аргументы. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|**Alias** <br/> |Строка, идентифицируемая для редактирования записи. Если аргумент  *Alias*  не указан, то текущая запись редактирована.  <br/> |
   
## <a name="remarks"></a>Примечания

После утверждения **EditRecord** можно вставить блок команд, которые будут выполняться до внесения изменений в запись. Следующие действия доступны в блоке **данных EditRecord.** 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[Если... Затем... Else Macro Statement](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Используйте действие **SetField,** чтобы указать новые значения поля в отредактируемой записи. 
  
Вы можете использовать **if... Затем... Другое** заявление для выполнения операций на основе условия. 
  
Чтобы отменить редактирование записи, используйте **действие CancelRecordChange.** Это предотвращает совершение изменений и выход из блока **данных EditRecord.** 
  
Для работы с последней записью, созданной в блоке данных CreateRecord, можно использовать локализованную переменную **LastCreateRecordIdentity.**  Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


