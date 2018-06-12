---
title: Функция Month (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Возвращает целое число, представляющее месяц указанной даты.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807090"
---
# <a name="month-function-access-custom-web-app"></a>Функция Month (приложение настраиваемых web Access)

Возвращает целое число, представляющее месяц указанной даты.
  
> [!NOTE]
> Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.* > Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **Месяц** (*Дата*) 
  
Функция **Month** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Дата*  <br/> |Выражение, которое разрешается в значение даты и времени.  <br/> |
   
## <a name="remarks"></a>Замечания

 **Месяц** возвращает совпадает со значением **DatePart** (месяц, дата). 
  
Если *Дата* содержит только часть времени, возвращаемое значение равно 1, базовый месяца. 
  

