---
title: Действия макроса SetField (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Действие SetField используется для присвоения значения поля.
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807115"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>Действия макроса SetField (приложение настраиваемых web Access)

Действие **SetField** используется для присвоения значения поля. 
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> **SetField** действие доступно только в макросов данных. 
  
## <a name="setting"></a>Параметр

Действие **SetField** содержит аргументы, перечисленные в следующей таблице. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
|**Name** <br/> |Строка, идентифицирующая поле.  <br/> |
|**Значение** <br/> |Выражение, которое задает значение, задаваемое в поле.  <br/> |
   
## <a name="remarks"></a>Замечания

Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block-access-custom-web-app.md)** или **[ИзменитьЗапись](editrecord-data-block-access-custom-web-app.md)** . 
  

