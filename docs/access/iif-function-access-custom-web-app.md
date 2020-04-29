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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439081"
---
# <a name="iif-function-access-custom-web-app"></a>Функция IIf (пользовательское веб-приложение для Access)

Проверяет, выполнено ли условие, и возвращает одно значение, если оно имеет значение FALSE.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**IIf** (*Condition*, *труевалуе*, *фалсевалуе*) 
  
Функция **IIf** содержит указанные ниже аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Условие*  <br/> |Выражение, которое требуется оценить.  <br/> |
| *труевалуе*  <br/> |Значение или выражение, возвращаемое, если *условие* имеет значение true.  <br/> |
| *фалсевалуе*  <br/> |Значение или выражение, возвращаемое, если *условие* имеет значение false.  <br/> |
   
## <a name="example"></a>Пример

Следующее выражение можно использовать для отображения полного имени пользователя, где в таблице содержатся поля FirstName, Миддлеинитиал и LastName. Если поле Миддлеинитиал не заполнено, только поля FirstName и LastName будут объединены для отображения полного имени.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


