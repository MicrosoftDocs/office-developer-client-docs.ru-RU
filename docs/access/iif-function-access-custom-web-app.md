---
title: Функция IIf (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Проверяет, срабатыет ли условие, и возвращает одно значение, если значение true для другого, если оно имеет значение FALSE.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439081"
---
# <a name="iif-function-access-custom-web-app"></a>Функция IIf (пользовательское веб-приложение Access)

Проверяет, срабатыет ли условие, и возвращает одно значение, если значение true для другого, если оно имеет значение FALSE.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**IIf** (*Condition,* *TrueValue*, *FalseValue*) 
  
Функция **IIf** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Condition*  <br/> |Выражение, которое вы хотите оценить.  <br/> |
| *TrueValue*  <br/> |Значение или выражение, возвращаемое,  *если условие*  имеет значение True.  <br/> |
| *FalseValue*  <br/> |Значение или выражение, возвращаемое,  *если условие*  имеет значение False.  <br/> |
   
## <a name="example"></a>Пример

Следующее выражение можно использовать для отображения полного имени человека, в котором таблица содержит поля FirstName, MiddleInitial и LastName. Если поле MiddleInitial пустое, для отображения полного имени объединяются только поля FirstName и LastName.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


