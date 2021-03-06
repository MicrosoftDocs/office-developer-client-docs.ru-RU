---
title: Функция count (Доступ к настраиваемой веб-приложении)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Возвращает количество записей в запросе или таблице.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419144"
---
# <a name="count-function-access-custom-web-app"></a>Функция count (Доступ к настраиваемой веб-приложении)

Возвращает количество записей в запросе или таблице.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**Count** *(Expression)* 
  
Функция **Count** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Expression*  <br/> |Строковая экспрессия, определяемая поле, содержаще данные, которые необходимо считать, или выражение, которое выполняет вычисление с помощью данных в поле. Operands в *Expression* может включать имя настольного поля или функции (которые могут быть внутренними или пользовательскими, но не другими SQL совокупными функциями). Можно вычислять любой тип данных, включая текст.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы вычислить количество записей в базовом запросе, можно использовать функцию Count. Например, можно использовать функцию Count для вычисления количества заказов, отправленных в определенную страну или регион.
  
**Count** \* () возвращает количество элементов в группе. Это включает значения nULL и дубликаты. 
  

