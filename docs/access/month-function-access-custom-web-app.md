---
title: Функция Month (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Возвращает целое число, представляющее месяц указанной даты.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308143"
---
# <a name="month-function-access-custom-web-app"></a>Функция Month (пользовательское веб-приложение для Access)

Возвращает целое число, представляющее месяц указанной даты.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **Month (месяц** ) (*Date*) 
  
Функция **Month** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Date*  <br/> |Выражение, которое может быть разрешено в значение даты и времени.  <br/> |
   
## <a name="remarks"></a>Замечания

 **Month** возвращает то же значение, что и **DatePart** (month, Date). 
  
Если *Дата* содержит только часть времени, возвращается значение 1, базовый месяц. 
  

