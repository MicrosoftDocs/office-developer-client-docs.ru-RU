---
title: Функция Coalesce (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Возвращает первое выражение, которое не является NULL, из списка аргументов.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411395"
---
# <a name="coalesce-function-access-custom-web-app"></a>Функция Coalesce (пользовательское веб-приложение Access)

Возвращает первое выражение, которое не является NULL, из списка аргументов.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**Coalesce** (*Value*, [*Value*], ...,[*Value*]) 
  
Функция **Coalesce** содержит следующие аргументы 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Значение*  <br/> |Выражение.  <br/> |
   
## <a name="remarks"></a>Примечания

Если все аргументы имеют значение NULL, **Coalesce** возвращает значение NULL. 
  
## <a name="example"></a>Пример

В качестве правила проверки для таблицы используется следующее выражение. Это выражение обеспечивает запись в полях "Имя", "Фамилия", "Электронная почта", "Мобильный телефон", "Рабочий телефон", "Домашний телефон" и "Компания" перед записью. Если любое из перечисленных полей оставлено пустым, функция **Coalesce** возвращает значение Null, что нарушает правило проверки. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


