---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Возврат значения даты, представленной года, месяца и дня отформатированное в соответствии с краткий формат в региональных параметрах компьютера. Значения для года, месяца и дня отражают григорианский календарь.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813566"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Возврат значения даты, представленной *год, месяц,* *день* и отформатированное в соответствии с краткий формат в региональных параметрах компьютера. Значения для *года*, *месяца* и *дня* отражают григорианский календарь. 
  
## <a name="syntax"></a>Синтаксис

Дата (** *год* **, ** *месяц* **, ** *день* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Обязательный  <br/> |**Integer** <br/> |Год.  <br/> |
| _month_ <br/> |Обязательный  <br/> |**Integer** <br/> |Месяц.  <br/> |
| _день_ <br/> |Обязательный  <br/> |**Integer** <br/> |День.  <br/> |
   
## <a name="example-1"></a>Пример 1

DATE(1999,6,7)
  
Возвращает значение, представляющее 6 и 7/1999 г.
  
## <a name="example-2"></a>Пример 2

Date(1999,6,7) + 4 ed.
  
Возвращает значение, представляющее 6/11/1999 г.
  
## <a name="example-3"></a>Пример 3

FORMAT(DATE(1999,10,14),"C")
  
Возвращает значение, представляющее вторник 14 октября 1999 г.
  

