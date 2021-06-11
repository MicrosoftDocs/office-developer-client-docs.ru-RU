---
title: Функция Concat (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Возвращает строку, которая является результатом объединения двух или более значений строки.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423274"
---
# <a name="concat-function-access-custom-web-app"></a>Функция Concat (Доступ к настраиваемой веб-приложению)

Возвращает строку, которая является результатом объединения двух или более значений строки.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**Concat** (*Value1*, *Value2*, ... [*ValueN*]) 
  
Функция **Concat** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
|Значение  <br/> |Значение строки, примыкает к другим значениям.  <br/> |
   
## <a name="remarks"></a>Примечания

**Concat** принимает переменную строку аргументов и соедает их в одну строку. Требуется минимум два аргумента строки; в противном случае будет поднята ошибка. 
  
Все аргументы неявно преобразуются в типы данных строки и затем согласуются.
  
## <a name="example"></a>Пример

Следующее выражение можно использовать для отображения полного имени человека, в котором таблица содержит поля FirstName, MiddleInitial и LastName. Если поле MiddleInitial пусто, для отображения полного имени объединяются только поля FirstName и LastName.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


