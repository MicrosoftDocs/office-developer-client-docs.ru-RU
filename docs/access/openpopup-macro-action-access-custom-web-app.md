---
title: OpenPopup Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Открывает указанное представление во всплывающее окно.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427390"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup Macro Action (пользовательское веб-приложение Access)

Открывает указанное представление во всплывающее окно.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **OpenPopup** (*View*, *Where=*, *Order By*) 
  
Действие **OpenPopup** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *View*  <br/> |Имя открываемого представления.  <br/> |
| *Where=*  <br/> |Допустимый SQL WHERE (без слова WHERE), ограничивающий записи в представлении.  <br/> |
| *Order By*  <br/> |Строка выражения, которая включает имя поля или полей, по которым необходимо сортировать записи, и необязательные ключевые слова ASC или DESC. По умолчанию этот аргумент пустой.  <br/> |
   
## <a name="remarks"></a>Примечания

Текущий макрос завершается после обработки действия **OpenPopup.** 
  
При наступлении действия **OpenPopup** любая сортировка или фильтрация, применяемая пользователем, очищается. 
  
Аргумент  *OrderBy*  — это имя поля или полей, по которым необходимо отсортировать записи. При использовании более одного имени поля разделять их запятой (,). 
  
При наборе  *аргумента OrderBy*  записи сортироваться по умолчанию в порядке возрастания. 
  

