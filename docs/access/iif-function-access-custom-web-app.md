---
title: Функция IIf (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Проверяет, будет ли условие соблюдено и возвращает одно значение, если значение TRUE, от друга в том случае, если оно равно FALSE.
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806933"
---
# <a name="iif-function-access-custom-web-app"></a>Функция IIf (приложение настраиваемых web Access)

Проверяет, будет ли условие соблюдено и возвращает одно значение, если значение TRUE, от друга в том случае, если оно равно FALSE.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**IIf** (*Условие*, *TrueValue*, *FalseValue*) 
  
Функция **IIf** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Условие*  <br/> |Выражение, которое требуется вычислить.  <br/> |
| *TrueValue*  <br/> |Значение или выражение, возвращаемое, если *условие* равно True.  <br/> |
| *FalseValue*  <br/> |Значение или выражение, возвращаемое, если *условие* равно False.  <br/> |
   
## <a name="example"></a>Пример

Следующее выражение можно использовать для отображения полного имени пользователя которых таблицы содержит полей FirstName, LastName и MiddleInitial. Если MiddleInitial поле не заполнено, чтобы отобразить полное имя объединяются только поля имя и Фамилия.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


