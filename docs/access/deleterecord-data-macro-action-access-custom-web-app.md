---
title: Макрокод DeleteRecord Data Macro (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Для удаления записи можно использовать действие DeleteRecord.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423155"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Макрокод DeleteRecord Data Macro (пользовательское веб-приложение Access)

Для удаления **записи можно использовать действие DeleteRecord.** 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="setting"></a>Параметр

Действие **DeleteRecord** имеет следующие аргументы. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|**Запись псевдонима** <br/> |Строка, идентифицирует запись, которую необходимо удалить. Если  *аргумент Alias*  не указан, текущая запись удаляется.  <br/> |
   
## <a name="remarks"></a>Примечания

Локализованную переменную **LastCreateRecordIdentity** можно использовать для работы с последней записью, созданной в блоке данных **CreateRecord.** Например, используйте следующий синтаксис для ссылки на недавно созданную запись: 
  
`[LastCreateRecordIdentity]`


