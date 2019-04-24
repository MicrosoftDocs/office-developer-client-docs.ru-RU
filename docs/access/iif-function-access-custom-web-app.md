---
title: Функция IIf (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Проверяет, выполнено ли условие, и возвращает одно значение, если оно имеет значение FALSE.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301864"
---
# <a name="iif-function-access-custom-web-app"></a>Функция IIf (пользовательское веб-приложение для Access)

Проверяет, выполнено ли условие, и возвращает одно значение, если оно имеет значение FALSE.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**IIf** (*Condition*, *труевалуе*, *фалсевалуе*) 
  
Функция **IIf** содержит указанные ниже аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Condition*  <br/> |Выражение, которое требуется оценить.  <br/> |
| *Труевалуе*  <br/> |Значение или выражение, возвращаемое, если *условие* имеет значение true.  <br/> |
| *Фалсевалуе*  <br/> |Значение или выражение, возвращаемое, если *условие* имеет значение false.  <br/> |
   
## <a name="example"></a>Пример

Следующее выражение можно использовать для отображения полного имени пользователя, где в таблице содержатся поля FirstName, Миддлеинитиал и LastName. Если поле Миддлеинитиал не заполнено, только поля FirstName и LastName будут объединены для отображения полного имени.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


