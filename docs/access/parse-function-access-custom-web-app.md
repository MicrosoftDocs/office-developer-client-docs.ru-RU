---
title: Функция parse (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Parses a text value and returns its value in a given type using the culture of the application.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411136"
---
# <a name="parse-function-access-custom-web-app"></a>Функция parse (Доступ к настраиваемой веб-приложению)

Parses a text value and returns its value in a given type using the culture of the application.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **Parse** *(TextExpression*, *DataType*) 
  
Функция **Parse** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *TextExpression*  <br/> |Текстовое выражение, представляющее отформатированные значения для анализа в указанный тип данных.  <br/> |
| *DataType*  <br/> |Буквальное значение, представляющее тип данных, запрашиваемого для результата.  <br/> |
   
## <a name="remarks"></a>Примечания

Используйте **Parse** только для преобразования из строки в дату и время и типы номеров. Для преобразований общего типа используйте функцию **Convert.** Имейте в виду, что существует определенная накладная часть производительности при разборе значения строки. 
  

