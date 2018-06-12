---
title: Функция TIME (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Возвращает время, представленные в час, минуты и секунды.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815044"
---
# <a name="time-function-visioshapesheet"></a>Функция TIME (VisioShapeSheet)

Возвращает время, представленное _часа_, _минуты_и _второй_.
  
## <a name="syntax"></a>Синтаксис

ВРЕМЯ (** *час* **, ** *минуту* **, ** *второй* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _час_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Компонент часов.  <br/> |
| _минуты_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Comonent минут.  <br/> |
| _секунды_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Второй компонент.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Числовой
  
## <a name="example-1"></a>Пример 1

TIME(15,30,30)
  
Возвращает значение, представляющее 15:30:30.
  
## <a name="example-2"></a>Пример 2

Format(Time(15,30,30),"hh:mm")
  
Возвращает значение, представляющее 15:30.
  
## <a name="example-3"></a>Пример 3

Time(15,30,30) + 8 а.
  
Возвращает значение, представляющее 23:30:30.
  

