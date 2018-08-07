---
title: Функция TRIM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Удаляет все пространство из текста, за исключением одиночных пробелов между словами.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815073"
---
# <a name="trim-function"></a>Функция TRIM

Удаляет все пространство из текста, за исключением одиночных пробелов между словами. 
  
## <a name="syntax"></a>Синтаксис

ОБРЕЗКА (** *текст* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**Строка** <br/> |Текст, из которого требуется удалить пробелы.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Можно использовать функцию СЖПРОБЕЛЫ на текст, полученный из другого приложения, которое может содержать избыточные пробелы.
  
## <a name="example"></a>Пример

ИСПОЛНЕНИЕ («1 января 2003») 
  
Возвращает «1 января 2003». 
  

