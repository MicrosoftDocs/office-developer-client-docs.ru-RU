---
title: Функция DateWithTimeFromParts (Доступ к пользовательскому веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Возвращает дату и время в зависимости от указанного года, месяца, дня и времени.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422091"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Функция DateWithTimeFromParts (Доступ к пользовательскому веб-приложению)

Возвращает дату и время в зависимости от указанного года, месяца, дня и времени.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**DateWithTimeFromParts** *(год,* *месяц,* *день,* *час,* *минута*, *секунда)* 
  
Функция **DateWithTimeFromParts** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Год*  <br/> |Integer expression specifying a year.  <br/> |
| *Month*  <br/> |Integer expression specifying a month.  <br/> |
| *Day*  <br/> |Integer expression specifying a day.  <br/> |
| *Hour*  <br/> |Integer expression specifying hours.  <br/> |
| *Minute*  <br/> |Integer expression specifying minutes.  <br/> |
| *Second*  <br/> |Integer expression specifying seconds.  <br/> |
   
## <a name="remarks"></a>Примечания

**DateWithTimeFromParts** возвращает полностью инициализированное значение Date/Time. Если аргументы не допустимы, вызывается ошибка. Если необходимые аргументы null, то Null возвращается. 
  

