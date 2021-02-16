---
title: Функция DatePart (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Возвращает числовом значении, которое представляет указанную часть даты указанной даты.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411437"
---
# <a name="datepart-function-access-custom-web-app"></a>Функция DatePart (пользовательское веб-приложение Access)

Возвращает числовом значении, которое представляет указанную часть даты указанной даты.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**DatePart** (*DatePart*, *Date*) 
  
Функция **DatePart** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *DatePart*  <br/> |Часть  *даты*  (значения даты или времени), для которой будет возвращено значение. Список допустимой аббревиатуры можно найти в разделе "Примечания".  <br/> |
| *Дата*  <br/> |Выражение, которое можно разрешить в значение даты и времени. Выражение  *аргумента Date,*  выражение столбца, определяемая пользователем переменная или строковый литерал.  <br/> |
   
## <a name="remarks"></a>Примечания

В следующей таблице перечислены все допустимые *аргументы DatePart.* 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**quarter** <br/> |
|**month** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**week** <br/> |
|**weekday** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**миллисекунд** <br/> |
   

