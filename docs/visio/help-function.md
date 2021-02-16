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
description: Открывает HTML-файл справки с закаленным ключевым словом в поле поиска.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431339"
---
# <a name="help-function"></a>Функция HELP

Открывает HTML-файл справки с закаленным  *ключевым*  словом в **поле** поиска. 
  
## <a name="syntax"></a>Синтаксис

HELP(" ** *filename.chm!keyword* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _filename.chm!keyword_ <br/> |Обязательно  <br/> |**Строка** <br/> | Имя файла справки и ключевое слово для поиска.  <br/> |
   
## <a name="remarks"></a>Примечания

Если  *ключевое*  слово не указано, функция HELP открывает страницу содержимого файла справки. 
  
## <a name="example"></a>Пример

HELP("visio.chm!shapesheet") 
  
Открывает файл справки Visio и отображает список тем, ключевое слово которых — shapesheet. 
  

