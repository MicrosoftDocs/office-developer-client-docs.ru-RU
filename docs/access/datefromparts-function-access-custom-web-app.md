---
title: Функция DateFromParts (Доступ к пользовательскому веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Возвращает значение даты за указанный год, месяц и день.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423225"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Функция DateFromParts (Доступ к пользовательскому веб-приложению)

Возвращает значение даты за указанный год, месяц и день.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**DateFromParts** *(Год,* *Месяц*, *День*) 
  
Функция **DateFromParts** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Год*  <br/> |Integer expression specifying a year.  <br/> |
| *Month*  <br/> |Integer expression specifying a month, from 1 to 12.  <br/> |
| *Day*  <br/> |Integer expression specifying a day.  <br/> |
   
## <a name="remarks"></a>Примечания

**DateFromParts** возвращает значение даты с указанной частью даты к указанному году, месяцу и дню и времени, заданным по умолчанию. Если аргументы не допустимы, то вызывается ошибка. Если необходимые аргументы являются null, NULL возвращается. 
  
## <a name="example"></a>Пример

Следующее выражение использует **функцию DateFromParts** для вычисления первого дня текущего месяца. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



