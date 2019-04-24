---
title: Функция HELP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Открывает HTML-файл справки с указанным ключевым словом в поле поиска.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329976"
---
# <a name="help-function"></a>Функция HELP

Открывает HTML-файл справки с указанным *ключевым словом* в поле **поиска** . 
  
## <a name="syntax"></a>Синтаксис

Справка ("* * *имя_файла. chm! ключевое слово* * *") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _filename. chm! ключевое слово_ <br/> |Обязательный  <br/> |**String** <br/> | Имя файла справки и ключевое слово для поиска.  <br/> |
   
## <a name="remarks"></a>Комментарии

Если *ключевое слово* не указано, функция Help открывает страницу содержимое файла справки. 
  
## <a name="example"></a>Пример

Справка ("Visio. chm! для таблицы свойств фигуры") 
  
Открывает файл справки по Visio и отображает список разделов с ключевым словом "Таблица свойств фигуры". 
  

