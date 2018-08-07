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
description: Открывает файл HTML-справки с ключевым словом указан в поле «Поиск».
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813899"
---
# <a name="help-function"></a>Функция HELP

Открывает файл HTML-справки с указанной *ключевое слово* в поле « **Поиск** ». 
  
## <a name="syntax"></a>Синтаксис

СПРАВКА ("** *filename.chm!keyword* **") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _filename.chm!Keyword_ <br/> |Обязательный  <br/> |**Строка** <br/> | Имя файла файл справки и ключевое слово для поиска.  <br/> |
   
## <a name="remarks"></a>Замечания

Если нет *ключевых слов* не указан, то функция справки открывает страницу содержимое файла справки. 
  
## <a name="example"></a>Пример

Help("Visio.chm!ShapeSheet") 
  
Открывает файл справки Visio и отображает список помеченным, чьи ключевое слово является «фигуры». 
  

