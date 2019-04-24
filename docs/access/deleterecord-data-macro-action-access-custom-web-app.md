---
title: Действие с макросами данных DeleteRecord (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Для удаления записи можно использовать действие DeleteRecord.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282117"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Действие с макросами данных DeleteRecord (пользовательское веб-приложение для Access)

Для удаления записи можно использовать действие **DeleteRecord** . 
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="setting"></a>Параметр

Макрокоманда **DeleteRecord** имеет следующие аргументы. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|**Псевдоним записи** <br/> |Строка, определяющая удаляемую запись. Если аргумент *Alias* не указан, то текущая запись удаляется.  <br/> |
   
## <a name="remarks"></a>Замечания

Локальную переменную **ласткреатерекордидентити** можно использовать для работы с последней записью, созданной в блоке данных **СоздатьЗапись** . Например, используйте следующий синтаксис для ссылки на последнюю созданную запись: 
  
`[LastCreateRecordIdentity]`


