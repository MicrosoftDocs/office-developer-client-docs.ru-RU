---
title: Функция TimeFromParts (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Возвращает значение времени на основе указанного частей.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807120"
---
# <a name="timefromparts-function-access-custom-web-app"></a>Функция TimeFromParts (приложение настраиваемых web Access)

Возвращает значение времени на основе указанного частей.
  
> [!NOTE]
> Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.* > Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **TimeFromParts** (*Час*, *минута* *второй*) 
  
Функция **TimeFromParts** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Час*  <br/> |Выражение целое число, указывающее часов.  <br/> |
| *Минуты*  <br/> |Выражение целое число, указывающее минут.  <br/> |
| *Секунды*  <br/> |Выражение целое число, указывающее секунд.  <br/> |
   
## <a name="see-also"></a>См. также

 **TimeFromParts** возвращает значение полностью инициализированный времени. Если недопустимые аргументы, возникает ошибка. Если параметры имеют значение null, возвращается значение null. 
  

