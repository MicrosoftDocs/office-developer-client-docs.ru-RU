---
title: Функция HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Возвращает значение TRUE, если указанная строка найдена в списке Категория фигуры.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813896"
---
# <a name="hascategory-function"></a>Функция HASCATEGORY

Возвращает значение TRUE, если указанная строка найдена в списке Категория фигуры.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

HASCATEGORY (** *категории* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _category_ <br/> |Обязательный  <br/> |**Строка** <br/> |Категории, которую требуется найти.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Boolean**
  
## <a name="remarks"></a>Замечания

 *Категории* являются пользовательских строк, которые можно использовать для упорядочивания фигур. Можно определить категории в ячейке User.msvShapeCategories в таблице свойств фигуры для фигуры. Можно определить нескольких категорий для фигуры на категории, разделив их точкой с запятой. 
  

