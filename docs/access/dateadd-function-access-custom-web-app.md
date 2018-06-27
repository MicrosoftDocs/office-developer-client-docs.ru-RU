---
title: Функция DateAdd (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Возвращает указанной даты с заданным интервалом номеров (целое положительное или отрицательное) добавлена части этой даты с указанной даты.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806971"
---
# <a name="dateadd-function-access-custom-web-app"></a>Функция DateAdd (приложение настраиваемых web Access)

Возвращает указанной даты с заданным интервалом номеров (целое положительное или отрицательное) добавлена части этой даты с указанной даты.
  
> [!NOTE]
> Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.* > Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**Функция DateAdd** (*DatePart*, *номер*, *Дата*) 
  
Функция **DateAdd** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *DatePart*  <br/> |Часть *даты* , к которому добавляется целое число. Обратитесь к "Примечания" для списка допустимых значений.  <br/> |
| *Число*  <br/> |— Это выражение, которое можно разрешить в целое число, добавляется в *указанной* *даты* . Если значение задано с помощью дробной, усекается дроби.  <br/> |
| *Дата*  <br/> |Выражение, которое разрешается в значение даты и времени. Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.  <br/> |
   
## <a name="remarks"></a>Замечания

В следующей таблице перечислены все допустимые аргументы *DatePart* . 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**квартал** <br/> |
|**month** <br/> |
|**DayOfYear** <br/> |
|**день** <br/> |
|**недели** <br/> |
|**час** <br/> |
|**минуты** <br/> |
|**секунды** <br/> |
|**мс** <br/> |
   
## <a name="example"></a>Пример

Следующее выражение вычисляет последний день текущего месяца.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

Следующее выражение вычисляет последний день предыдущего месяца.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`

