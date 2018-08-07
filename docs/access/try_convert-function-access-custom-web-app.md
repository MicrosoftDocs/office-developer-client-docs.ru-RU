---
title: Функция Try_Convert (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Преобразует значение указанного типа данных или возвращает значение Null, если преобразования не является допустимым.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807149"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Функция Try_Convert (приложение настраиваемых web Access)

Преобразует значение указанного типа данных или возвращает значение Null, если преобразования не является допустимым.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Try_Convert** (*Тип данных*, *выражение*) 
  
Функция **Try_Convert** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *DataType*  <br/> |Тип данных, в котором для преобразования *выражения* .  <br/> |
| *Выражение*  <br/> |Значение для преобразования.  <br/> |
   
## <a name="remarks"></a>Замечания

 **Try_Convert** принимает значение, переданное в нее и пытается преобразовать его для указанного *типа данных* . Если преобразование завершается успешно, **Try_Convert** возвращает значение как указанный *тип данных* ; Если возникает ошибка, возвращается значение null. Однако при запросе преобразования, явно не разрешено **Try_Convert** сбой с ошибкой. 
  

