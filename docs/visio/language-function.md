---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Позволяет выполнять операции сравнения между представлениями другой язык. Она лучше всего использовать для преобразования значений тегов (BCP 47) язык Internet инженерной рабочей группы в значения id (LCID) для языкового стандарта.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814052"
---
# <a name="language-function"></a>LANGUAGE Function

Позволяет выполнять операции сравнения между представлениями другой язык. Она лучше всего использовать для преобразования значений тегов (BCP 47) язык Internet инженерной рабочей группы в значения id (LCID) для языкового стандарта.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **Язык** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Обязательный  <br/> |**Строка** <br/> |Код языка или BCP 47 значение языка.  <br/> |
   
## <a name="return-value"></a>������������ ��������

Целое число
  
## <a name="example"></a>Пример

 `LANGUAGE("en-us")`
  
Возвращает значение "1033".
  
 `LANGUAGE("es-es")`
  
Возвращает значение "3082".
  

