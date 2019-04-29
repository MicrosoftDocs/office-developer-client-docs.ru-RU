---
title: Макрокоманда SetField (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Действие SetField можно использовать для присвоения значения полю.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432928"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>Макрокоманда SetField (пользовательское веб-приложение для Access)

Действие **SetField** можно использовать для присвоения значения полю. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Действие **SetField** доступно только в макросах данных. 
  
## <a name="setting"></a>Setting

Макрокоманда **SetField** содержит аргументы, приведенные в следующей таблице. 
  
|**Имя аргумента**|**Description**|
|:-----|:-----|
|**Name** <br/> |Строка, определяющая поле.  <br/> |
|**Значение** <br/> |Выражение, задающее значение, присваиваемое полю.  <br/> |
   
## <a name="remarks"></a>Примечания

Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block-access-custom-web-app.md)** или **[ИзменитьЗапись](editrecord-data-block-access-custom-web-app.md)** . 
  

