---
title: Функция EOMonth (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Возвращает последний день месяца до или указанное количество месяцев.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437457"
---
# <a name="eomonth-function-access-custom-web-app"></a>Функция EOMonth (Доступ к настраиваемой веб-приложению)

Возвращает последний день месяца до или указанное количество месяцев.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **EOMonth** (*Дата*, *NumberOfMonth*) 
  
**EOMonth содержит** следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Date*  <br/> |Дата начала в формате Date/Time или в принятом текстовом представлении даты.  <br/> |
| *NumberOfMonth*  <br/> |Число, представляющее число месяцев до или после  *даты*  .  <br/> |
   
## <a name="remarks"></a>Примечания

Если  *дата*  не является допустимой датой, **EOMonth** возвращает ошибку. 
  
Если  *Date*  plus  *NumberOfMonth*  дает недействительные даты, **EOMonth** возвращает ошибку. 
  

