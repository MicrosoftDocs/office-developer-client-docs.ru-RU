---
title: Функция объединения функции (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Возвращает первое выражение, которое не имеет значение NULL, из списка аргументов.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806955"
---
# <a name="coalesce-function-access-custom-web-app"></a>Функция объединения функции (приложение настраиваемых web Access)

Возвращает первое выражение, которое не имеет значение NULL, из списка аргументов.
  
> [!NOTE]
> Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.* > Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

**Функция объединения** (*Значение*, [*значение*],..., [*значение*]) 
  
Функция **Объединение** содержит следующие аргументы 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Значение*  <br/> |Выражение.  <br/> |
   
## <a name="remarks"></a>Замечания

Если все аргументы имеют значение NULL, **Объединение** возвращает значение NULL. 
  
## <a name="example"></a>Пример

Следующее выражение используется как правила проверки для таблицы. Выражение гарантирует, что записи вносятся в поля имя, последнее имя электронной почты, мобильный телефон, рабочего телефона, домашней телефона, и компаниями перед сохранением записи. Если какие-либо из перечисленных полей незаполненными, функция **объединения** возвращает Null, которые нарушают правило проверки. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```

