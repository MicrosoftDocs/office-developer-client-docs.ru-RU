---
title: Функция DateFromParts (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Возвращает значение типа date для указанного года, месяца и дня.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806917"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Функция DateFromParts (приложение настраиваемых web Access)

Возвращает значение типа date для указанного года, месяца и дня.
  
> [!NOTE]
> Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.* > Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**DateFromParts** (*Год*, *месяц*, *день*) 
  
Функция **DateFromParts** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Year*  <br/> |Выражение целое число, указывающее года.  <br/> |
| *Month*  <br/> |Выражение целое число, указывающее месяц, от 1 до 12.  <br/> |
| *Day*  <br/> |Выражение целое число, указывающее день.  <br/> |
   
## <a name="remarks"></a>Замечания

**DateFromParts** возвращает значение типа date с области даты, задайте для указанного года, месяца и дня и области времени, значение по умолчанию. Если аргументы не допускаются, возникает ошибка. При необходимости, что аргументы имеют значение null, возвращается значение NULL. 
  
## <a name="example"></a>Пример

Следующее выражение использует функцию **DateFromParts** для вычисления с первого дня текущего месяца. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



