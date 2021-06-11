---
title: Try_Parse Function (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Парсирует текстовое значение указанного типа данных в культуре приложения или возвращает Null, если преобразование не допустимо.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427530"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse Function (Доступ к настраиваемой веб-приложению)

Парсирует текстовое значение указанного типа данных в культуре приложения или возвращает Null, если преобразование не допустимо.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **Try_Parse** *(TextExpression*, *DataType*) 
  
Функция **Try_Parse** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *TextExpression*  <br/> |Текстовое выражение, представляющее отформатированные значения для анализа в указанный тип данных.  <br/> |
| *DataType*  <br/> |Тип данных, в который можно разрезать  *TextExpression*  .  <br/> |
   
## <a name="remarks"></a>Примечания

Используйте **Try_Parse** только для преобразования из строки в дату/время и типы номеров. Для преобразований общего типа продолжайте использовать **Convert**. 
  

