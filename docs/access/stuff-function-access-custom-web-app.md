---
title: Функция stuff (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Вставляет текстовую строку в другую текстовую строку. Он удаляет указанную длину символов в первой строке в начале позиции, а затем вставляет вторую строку в первую строку в начале позиции.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427677"
---
# <a name="stuff-function-access-custom-web-app"></a>Функция stuff (Доступ к настраиваемой веб-приложению)

Вставляет текстовую строку в другую текстовую строку. Он удаляет указанную длину символов в первой строке в начале позиции, а затем вставляет вторую строку в первую строку в начале позиции.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Stuff** *(IntoTextExpression,* *Start*, *Length*, *ThisTextExpression*) 
  
Функция **Stuff** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Текстовое выражение, которое указывает текст, в который будет вставлен текст, указанный *в ThisTextExpression.*  <br/> |
| *Start*  <br/> |Integer value that specifies the location to start deletion and insertion. Если начало или длина отрицательные, возвращается строка null. Если начало больше, чем первая  *строка IntoTextExpression,*  возвращается null string.  <br/> |
| *Length*  <br/> |Integer, который указывает количество символов для удаления. Если длина больше, чем первая  *IntoTextExpression,*  удаление происходит до последнего символа в последнем  *IntoTextExpression*  .  <br/> |
| *ThisTextExpression*  <br/> |В шляпе текстового выражения указывается текст, который необходимо вставить *в IntoTextExpression.* Это выражение заменит длинные символы  *IntoTextExpression, начиная*  со  *старта*  .  <br/> |
   
## <a name="remarks"></a>Примечания

Если *аргументы "Начало"* или "Длина" являются отрицательными или если начальная позиция больше длины первой строки, возвращается строка null.  Если стартовая позиция 0, возвращается значение null. Если длина удаления больше, чем первая строка, она удаляется первому символу в первой строке. 
  

