---
title: EditRecord Data Block (Access custom web app)
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
# <a name="editrecord-data-block-access-custom-web-app"></a>EditRecord Data Block (Access custom web app)

Блок данных **EditRecord можно** использовать для изменения значений, содержащихся в существующей записи. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Блок **данных EditRecord** доступен только в макросах данных. 
  
## <a name="setting"></a>Setting

Блок **данных EditRecord** имеет следующие аргументы. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|**Alias** <br/> |Строка, идентифицирует запись, которую необходимо изменить. Если  *аргумент Alias*  не указан, то текущая запись будет изменена.  <br/> |
   
## <a name="remarks"></a>Примечания

После выполнения **команды EditRecord** можно вставить блок команд, которые будут выполняться до того, как будут зафиксированы изменения записи. В блоке данных **EditRecord** доступны следующие действия. 
  
||
|:-----|
|[CancelRecordChange Macro Action](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment Macro Statement](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group Macro Statement](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Затем... Else Macro Statement](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField Macro Action](setfield-macro-action-access-custom-web-app.md) <br/> |
|[SetLocalVar Macro Action](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Используйте действие **SetField,** чтобы указать новые значения поля в измененной записи. 
  
Вы можете использовать **if... Затем... Заявление Else** для выполнения операций на основе условия. 
  
Чтобы отменить редактирование записи, используйте действие **CancelRecordChange.** Это предотвращает зафиксирование изменений и выход из блока данных **EditRecord.** 
  
Локализованную переменную **LastCreateRecordIdentity** можно использовать для работы с последней записью, созданной в блоке данных **CreateRecord.** Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


