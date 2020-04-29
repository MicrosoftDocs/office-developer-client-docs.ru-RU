---
title: Функция Try_Convert (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Преобразует значение в указанный тип данных или возвращает значение null, если преобразование является недопустимым.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410898"
---
# <a name="try_convert-function-access-custom-web-app"></a>Функция Try_Convert (пользовательское веб-приложение для Access)

Преобразует значение в указанный тип данных или возвращает значение null, если преобразование является недопустимым.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Try_Convert** (*DataType*, *Expression*) 
  
Функция **Try_Convert** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *DataType*  <br/> |Тип данных, в который преобразуется *выражение* .  <br/> |
| *Expression*  <br/> |Преобразуемое значение.  <br/> |
   
## <a name="remarks"></a>Примечания

 **Try_Convert** получает значение, переданное в него, и пытается преобразовать его в указанный *тип данных* . Если преобразование завершается успешно, **Try_Convert** возвращает значение в виде указанного *типа данных* ; При возникновении ошибки возвращается значение null. Тем не менее, если вы запрашиваете явное преобразование, то **Try_Convert** завершается с ошибкой. 
  

