---
title: Функция CharIndex (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Поиск выражения текст для другого выражения текста и возвращает его запуск позиция, если найти.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806968"
---
# <a name="charindex-function-access-custom-web-app"></a>Функция CharIndex (приложение настраиваемых web Access)

Поиск выражения текст для другого выражения текста и возвращает его запуск позиция, если найти.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**CharIndex** (*TextExpression*, *WithinText*[*Пуск*]) 
  
|**Имя аргумента**|**Обязательное**|**Описание**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Да  <br/> |Выражение текст, который содержит текст для поиска.  <br/> |
| *WithinText*  <br/> |Да  <br/> |Выражения текст для поиска.  <br/> |
| *Start*  <br/> |Нет  <br/> |Целое число, задающее расположение в *WithinText* , чтобы начать поиск. Если *запустить* не указан, имеет отрицательное значение или равен 0, поиск начинается в начале *WithinText* .  <br/> |
   
## <a name="remarks"></a>Замечания

Если *TextExpression* или *WithinText* имеет значение NULL, *CharIndex* возвращает NULL. 
  
Если *TextExpression* не найден в *WithinText*, *CharIndex* возвращает значение 0. 
  
Позицию возвращаемой 1, а не от нуля.
  

